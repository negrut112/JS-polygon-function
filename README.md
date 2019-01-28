<h1><a id="JSpolygonfunction_0"></a>JS-polygon-function</h1>

<p>I’ve used the HTML and JavaScript to draw a polygon using 4 parameters: sides number, side size and two for starting point wich is middle.</p>
<p>You can acces the live preview on: <a href="https://negrut112.github.io/JS-polygon-function/">https://negrut112.github.io/JS-polygon-function/</a><br>
<img src="https://i.imgur.com/R2H9piQ.jpg"><br>
<b>HTML</b>
<p>I have used the HTML to define the area where I’m working defining the height, width and the border style:</p>
<p>&lt;canvas id=“myCanvas” height=“310” width=“500” style=“border: 1px solid black”&gt;&lt;/canvas&gt;</p>
<b>JavaScript</b>
<p>As you can see we have 7 polygons, I made a function for the unfilled ones and a separate one for the filled one. then I displayed them using console.log(); according to my needs.<br>
I will show you the filled function and what’s different from the other one below:</p>
<pre><code>function polygonf(sides1, size1, X1, Y1){
context.strokeStyle = &quot;orange&quot;;
context.stroke();
context.beginPath();
context.moveTo (X1 +  size1 * Math.cos(0), Y1 +  size1 *  Math.sin(0));  
for (var i = 1; i &lt;= sides1;i += 1) {
context.lineTo (X1 + size1 * Math.cos(i * 2 * Math.PI / sides1), Y1 + size1 * Math.sin(i * 2 * Math.PI / sides1));
context.fillStyle = &quot;orange&quot;; // The difference is &quot;fillStyle&quot; method.
context.fill();
</code></pre>
<p>};<br>
};</p>
<br>
Here is what I console.log-ed <br>
console.log(polygon(6,40,225,150)); //center one<br>
console.log(polygonf(6,40,290,187.5)); //the filled one
