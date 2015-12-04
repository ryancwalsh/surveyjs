---
layout: example
title: Use properties to set up your survey
---
<p>
Question Required Text: <input type="text" value="* " onChange="survey.requiredText = this.value; survey.render();"/> default is "* ".
<pre class="brush:js">survey.requiredText = yourValue; survey.render();</pre>
</p>
<p>
Show Question Numbers: <select onChange="survey.showQuestionNumbers = this.value; survey.render();">
    <option value="on" selected="true">on</option>
    <option value="onPage">onPage</option>
    <option value="off">off</option>
</select> default is 'on'. 'onPage' - set question numbers inside one page.
<pre class="brush:js">survey.showQuestionNumbers = yourValue; survey.render();</pre>
</p>
<p>
Show Title: <input type="checkbox" checked="true" onChange="survey.showTitle = this.checked; survey.render();"/> default is true.
<pre class="brush:js">survey.showTitle = yourValue; survey.render();</pre>
</p>
Show Page Titles: <input type="checkbox" checked="true" onChange="survey.showPageTitles = this.checked; survey.render();"/> default is true.
<pre class="brush:js">survey.showPageTitles = yourValue; survey.render();</pre>
<p>
Show Page Numbers: <input type="checkbox" onChange="survey.showPageNumbers = this.checked; survey.render();"/> default is false.
<pre class="brush:js">survey.showPageNumbers = yourValue; survey.render();</pre>
</p>
{% capture survey_setup %}
var survey = new Survey.Survey({% include surveys/survey-severalpages.json %});
{% endcapture %}

{% include live-example-code.html %}