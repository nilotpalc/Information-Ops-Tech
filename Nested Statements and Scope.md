---


---

<h1 id="scope">Scope</h1>
<p>The <code>scope</code> concept indicates that any variable assigned within the function or indentation will impact the lower indentation and not the prior functions or higher indent</p>
<p>Python evaluates variables on the <strong>LEGB</strong> rule.<br>
<strong>L</strong>: Local — Names assigned in any way within a function (def or lambda), and not declared global in that function.<br>
<strong>E</strong>: Enclosing function locals — Names in the local scope of any and all enclosing functions (def or lambda), from inner to outer.<br>
<strong>G</strong>: Global (module) — Names assigned at the top-level of a module file, or declared global in a def within the file.<br>
<strong>B</strong>: Built-in (Python) — Names preassigned in the built-in names module : open, range, SyntaxError,…</p>
<p>Example to explain how the variable assignment works -</p>
<pre class=" language-python"><code class="prism  language-python">x <span class="token operator">=</span> <span class="token number">50</span>

<span class="token keyword">def</span> <span class="token function">func</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">:</span>
    <span class="token keyword">global</span> x
    <span class="token keyword">print</span><span class="token punctuation">(</span><span class="token string">'This function is now using the global x!'</span><span class="token punctuation">)</span>
    <span class="token keyword">print</span><span class="token punctuation">(</span><span class="token string">'Because of global x is: '</span><span class="token punctuation">,</span> x<span class="token punctuation">)</span>
    x <span class="token operator">=</span> <span class="token number">2</span>
    <span class="token keyword">print</span><span class="token punctuation">(</span><span class="token string">'Ran func(), changed global x to'</span><span class="token punctuation">,</span> x<span class="token punctuation">)</span>

<span class="token keyword">print</span><span class="token punctuation">(</span><span class="token string">'Before calling func(), x is: '</span><span class="token punctuation">,</span> x<span class="token punctuation">)</span>
func<span class="token punctuation">(</span><span class="token punctuation">)</span>
<span class="token keyword">print</span><span class="token punctuation">(</span><span class="token string">'Value of x (outside of func()) is: '</span><span class="token punctuation">,</span> x<span class="token punctuation">)</span>
</code></pre>
<p>The output of this code is as follows -</p>
<blockquote>
<p>Before calling func(), x is:  50<br>
This function is now using the global x!<br>
Because of global x is:  50<br>
Ran func(), changed global x to 2<br>
Value of x (outside of func()) is:  2</p>
</blockquote>
<p>The key highlights of this code and variable assignment is as follows -</p>
<ol>
<li>The first line of code that runs is <code>print('Before calling func(), x is: ', x)</code>. This takes the value of x as the global x = 50</li>
<li>The second code that runs is <code>func()</code>
<ol>
<li>The first 2 statements run with global x value as nothing has been defined in the prior levels</li>
<li>The last code looks at identifying x and then,
<ol>
<li>Understands there is the global variable x as defined by the use of the code <code>global</code></li>
<li>Runs the function <code>func()</code> and determines x = 2</li>
</ol>
</li>
<li>Once the whole function runs, the value of x now stands at 2</li>
</ol>
</li>
</ol>
<blockquote>
<p>Key Point to Note: Use separate variable names throughout the code except when we want to change the value of a variable in the function</p>
</blockquote>
<p>The detailed forms of coding statements and challenges are covered in this gist.github <a href="https://gist.github.com/nilotpalc/d2623b6ab9206eb2cb7759190c198e96">file link</a></p>

