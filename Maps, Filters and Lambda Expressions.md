---


---

<h1 id="maps">Maps</h1>
<p>Map function <strong>runs the listed function across all the items in a list</strong> and returns the results in the form of a list. However, it is similar to a generator function and does not provide a direct output.<br>
The map function needs to be used along with the list function to generate a usable output<br>
<strong>Also, do not use <code>()</code> bracket in front of the function within the map expression</strong></p>
<pre class=" language-python"><code class="prism  language-python"><span class="token builtin">map</span><span class="token punctuation">(</span>functioname<span class="token punctuation">,</span> listname<span class="token punctuation">)</span>
<span class="token builtin">list</span><span class="token punctuation">(</span><span class="token builtin">map</span><span class="token punctuation">(</span>functionname<span class="token punctuation">,</span> listname<span class="token punctuation">)</span><span class="token punctuation">)</span>
</code></pre>
<h1 id="filter">Filter</h1>
<p>Filter function runs the input on all the values of the list and returns all items in the list that meet the <code>True</code> condition of the pre-defined function.<br>
<strong>Also, do not use <code>()</code> bracket in front of the function within the map expression</strong></p>
<pre class=" language-python"><code class="prism  language-python"><span class="token builtin">filter</span><span class="token punctuation">(</span>functionname<span class="token punctuation">,</span> listname<span class="token punctuation">)</span>
<span class="token builtin">list</span><span class="token punctuation">(</span><span class="token builtin">filter</span><span class="token punctuation">(</span>functionname<span class="token punctuation">,</span> listname<span class="token punctuation">)</span><span class="token punctuation">)</span>
</code></pre>
<blockquote>
<p>Note: The functionname in filter` needs to <strong>return a value as True or False</strong>.<br>
Or else, the filter function will not work</p>
</blockquote>
<h1 id="lambda-expression">Lambda Expression</h1>
<p>The lambda expression is primarily used to run small expressions that need to be run one time within the code and need not be saved as functions. This will primarily be used for similar functions.<br>
Example of a variable being squared</p>
<pre class=" language-python"><code class="prism  language-python"><span class="token keyword">lambda</span> variablename<span class="token punctuation">:</span> variablename <span class="token operator">**</span><span class="token number">2</span>
</code></pre>
<p>The lambda expression can also be assigned a variable name but, it generally used as one of the inputs with other functions like <code>map</code> and <code>filter</code></p>
<pre class=" language-python"><code class="prism  language-python"><span class="token comment"># returns a list of squared numbers</span>
<span class="token comment"># included in listname</span>
<span class="token builtin">list</span><span class="token punctuation">(</span><span class="token builtin">map</span><span class="token punctuation">(</span><span class="token keyword">lambda</span> num<span class="token punctuation">:</span> num<span class="token operator">**</span><span class="token number">2</span><span class="token punctuation">,</span> listname<span class="token punctuation">)</span><span class="token punctuation">)</span>

<span class="token comment"># returns a filtered list showing </span>
<span class="token comment"># even numbers within listname</span>
<span class="token builtin">list</span><span class="token punctuation">(</span><span class="token builtin">filter</span><span class="token punctuation">(</span><span class="token keyword">lambda</span> num<span class="token punctuation">:</span> num <span class="token operator">%</span> <span class="token number">2</span> <span class="token operator">==</span> <span class="token number">0</span><span class="token punctuation">,</span> listname<span class="token punctuation">)</span><span class="token punctuation">)</span>
</code></pre>

