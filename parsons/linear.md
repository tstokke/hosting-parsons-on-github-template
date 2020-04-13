---
title: Linear Search 4
layout: default
---

Organize the blocks so that there is a function that performs a linear search.
The function will be called from main, with it's returned value displayed on the screen.

<div id="sortableTrash" class="sortable-code"></div> 
<div id="sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="feedbackLink" value="Get Feedback" type="button" /> 
    <input id="newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "def findNumberGreaterThan10(theList):\n" +
    "   count = 0\n" +
    "   for value in theList:\n" +
    "      if value > 10:\n" +
    "         count = count + 1\n" +
    "   return count\n" +
    "def main():\n" +
    "   numbers = [3, 12, 4, 10, 9, 20, 7]\n" +
    "   numGreaterThan10 = findNumberGreaterThan10(numbers)\n" +
    "   print (\"Number of values > 10\", numGreaterThan10)\n" +
    "main()   ";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "sortable",
    "max_wrong_lines": 1,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>
