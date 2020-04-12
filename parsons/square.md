---
layout: default
title: Multiple Parson's Problems on One Page
---
<div id="Sample Parson's Problems-sortableTrash" class="sortable-code"></div> 
<div id="Sample Parson's Problems-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="Sample Parson's Problems-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="Sample Parson's Problems-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
  var initial = "def square (a):\n" +
    "   return a * a\n" +
    "def main()\n" +
    "   side = 10\n" +
    "   squared = square (side)\n" +
    "   print (\"Squared area is \", squared)\n" +
    "main()";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "Sample Parson's Problems-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#Sample Parson's Problems-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#Sample Parson's Problems-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
</script>
