# WeIrD-StRiNg-CaSe
Solution to WeIrD StRiNg CaSe algorithm question on Codewars.

Write a function toWeirdCase (weirdcase in Ruby) that accepts a string, and returns the same string with all even indexed characters in each word upper cased, and all odd indexed characters in each word lower cased. The indexing just explained is zero based, so the zero-ith index is even, therefore that character should be upper cased and you need to start over for each word.

The passed in string will only consist of alphabetical characters and spaces(' '). Spaces will only be present if there are multiple words. Words will be separated by a single space(' ').

Examples:
toWeirdCase( "String" );//=> returns "StRiNg"
toWeirdCase( "Weird string case" );//=> returns "WeIrD StRiNg CaSe"
<br>
__________________________________________________________________

<strong>Solution</strong>

function toWeirdCase(string){<br>
&nbsp;&nbsp;let ans=[]<br>
&nbsp;&nbsp;let count=0<br>
&nbsp;&nbsp;string.toLowerCase().split('').forEach((value , i)=>{<br>
&nbsp;&nbsp;&nbsp;if(count==0 || count%2==0) ans.push(value.toUpperCase())  <br>
&nbsp;&nbsp;&nbsp;else ans.push(value)    <br>
&nbsp;&nbsp;&nbsp;count++     <br>
&nbsp;&nbsp;&nbsp;if(value==' ') count=0    <br>
&nbsp;&nbsp;&nbsp;})<br>
&nbsp;&nbsp;ans=ans.join('')<br>
&nbsp;&nbsp;return ans<br>
}<br>
