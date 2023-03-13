---
keywords: fastai
title: JavaScript UI Development
toc: true 
badges: true
comments: true
categories: [PBL]
nb_path: _notebooks/2022-09-25-javascript-data.ipynb
layout: notebook
---

<!--
#################################################
### THIS FILE WAS AUTOGENERATED! DO NOT EDIT! ###
#################################################
# file to edit: _notebooks/2022-09-25-javascript-data.ipynb
-->

<div class="container" id="notebook-container">
        
    {% raw %}
    
<div class="cell border-box-sizing code_cell rendered">
<div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-javascript"><pre><span></span><span class="nx">console</span><span class="p">.</span><span class="nx">log</span><span class="p">(</span><span class="s2">&quot;Hi&quot;</span><span class="p">);</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">

<div class="output_area">

<div class="output_subarea output_stream output_stdout output_text">
<pre>Hi
</pre>
</div>
</div>

</div>
</div>

</div>
    {% endraw %}

    {% raw %}
    
<div class="cell border-box-sizing code_cell rendered">
<div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-javascript"><pre><span></span><span class="kd">function</span> <span class="nx">logItType</span><span class="p">(</span><span class="nx">output</span><span class="p">)</span> <span class="p">{</span>
    <span class="nx">console</span><span class="p">.</span><span class="nx">log</span><span class="p">(</span><span class="k">typeof</span> <span class="nx">output</span><span class="p">,</span> <span class="s2">&quot;;&quot;</span><span class="p">,</span> <span class="nx">output</span><span class="p">);</span> <span class="c1">//&quot;typeof&quot; keyword returns the type.</span>
<span class="p">}</span>
</pre></div>

    </div>
</div>
</div>

</div>
    {% endraw %}

    {% raw %}
    
<div class="cell border-box-sizing code_cell rendered">
<div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-javascript"><pre><span></span><span class="kd">function</span> <span class="nx">Person</span><span class="p">(</span><span class="nx">name</span><span class="p">,</span> <span class="nx">email</span><span class="p">,</span> <span class="nx">classOf</span><span class="p">)</span> <span class="p">{</span>
    <span class="k">this</span><span class="p">.</span><span class="nx">name</span> <span class="o">=</span> <span class="nx">name</span><span class="p">;</span>
    <span class="k">this</span><span class="p">.</span><span class="nx">email</span> <span class="o">=</span> <span class="nx">email</span><span class="p">;</span>
    <span class="k">this</span><span class="p">.</span><span class="nx">classOf</span> <span class="o">=</span> <span class="nx">classOf</span><span class="p">;</span>
    <span class="k">this</span><span class="p">.</span><span class="nx">role</span> <span class="o">=</span> <span class="s2">&quot;&quot;</span><span class="p">;</span>
<span class="p">}</span>

<span class="nx">Person</span><span class="p">.</span><span class="nx">prototype</span><span class="p">.</span><span class="nx">setRole</span> <span class="o">=</span> <span class="kd">function</span><span class="p">(</span><span class="nx">role</span><span class="p">)</span> <span class="p">{</span>
    <span class="k">this</span><span class="p">.</span><span class="nx">role</span> <span class="o">=</span> <span class="nx">role</span><span class="p">;</span>
<span class="p">}</span>

<span class="nx">Person</span><span class="p">.</span><span class="nx">prototype</span><span class="p">.</span><span class="nx">toJSON</span> <span class="o">=</span> <span class="kd">function</span><span class="p">()</span> <span class="p">{</span>
    <span class="kr">const</span> <span class="nx">obj</span> <span class="o">=</span> <span class="p">{</span><span class="nx">name</span><span class="o">:</span> <span class="k">this</span><span class="p">.</span><span class="nx">name</span><span class="p">,</span> <span class="nx">ghID</span><span class="o">:</span> <span class="k">this</span><span class="p">.</span><span class="nx">email</span><span class="p">,</span> <span class="nx">classOf</span><span class="o">:</span> <span class="k">this</span><span class="p">.</span><span class="nx">classOf</span><span class="p">,</span> <span class="nx">role</span><span class="o">:</span> <span class="k">this</span><span class="p">.</span><span class="nx">role</span><span class="p">};</span>
    <span class="kr">const</span> <span class="nx">json</span> <span class="o">=</span> <span class="nx">JSON</span><span class="p">.</span><span class="nx">stringify</span><span class="p">(</span><span class="nx">obj</span><span class="p">);</span>
    <span class="k">return</span> <span class="nx">json</span><span class="p">;</span>
<span class="p">}</span>

<span class="c1">// make a new Person and assign to variable teacher</span>
<span class="kd">var</span> <span class="nx">teacher</span> <span class="o">=</span> <span class="k">new</span> <span class="nx">Person</span><span class="p">(</span><span class="s2">&quot;Mr M&quot;</span><span class="p">,</span> <span class="s2">&quot;jmortensen@powayusd.com&quot;</span><span class="p">,</span> <span class="mf">1977</span><span class="p">);</span>  <span class="c1">// object type is easy to work with in JavaScript</span>
<span class="nx">logItType</span><span class="p">(</span><span class="nx">teacher</span><span class="p">);</span>  <span class="c1">// before role</span>
<span class="nx">logItType</span><span class="p">(</span><span class="nx">teacher</span><span class="p">.</span><span class="nx">toJSON</span><span class="p">());</span>  <span class="c1">// ok to do this even though role is not yet defined</span>

<span class="c1">// output of Object and JSON/string associated with Teacher</span>
<span class="nx">teacher</span><span class="p">.</span><span class="nx">setRole</span><span class="p">(</span><span class="s2">&quot;Teacher&quot;</span><span class="p">);</span>   <span class="c1">// set the role</span>
<span class="nx">logItType</span><span class="p">(</span><span class="nx">teacher</span><span class="p">);</span> 
<span class="nx">logItType</span><span class="p">(</span><span class="nx">teacher</span><span class="p">.</span><span class="nx">toJSON</span><span class="p">());</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">

<div class="output_area">

<div class="output_subarea output_stream output_stdout output_text">
<pre>object ; Person {
  name: &#39;Mr M&#39;,
  email: &#39;jmortensen@powayusd.com&#39;,
  classOf: 1977,
  role: &#39;&#39; }
string ; {&#34;name&#34;:&#34;Mr M&#34;,&#34;ghID&#34;:&#34;jmortensen@powayusd.com&#34;,&#34;classOf&#34;:1977,&#34;role&#34;:&#34;&#34;}
object ; Person {
  name: &#39;Mr M&#39;,
  email: &#39;jmortensen@powayusd.com&#39;,
  classOf: 1977,
  role: &#39;Teacher&#39; }
string ; {&#34;name&#34;:&#34;Mr M&#34;,&#34;ghID&#34;:&#34;jmortensen@powayusd.com&#34;,&#34;classOf&#34;:1977,&#34;role&#34;:&#34;Teacher&#34;}
</pre>
</div>
</div>

</div>
</div>

</div>
    {% endraw %}

    {% raw %}
    
<div class="cell border-box-sizing code_cell rendered">
<div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-javascript"><pre><span></span><span class="kd">var</span> <span class="nx">students</span> <span class="o">=</span> <span class="p">[</span> 
    <span class="k">new</span> <span class="nx">Person</span><span class="p">(</span><span class="s2">&quot;Krish Patil&quot;</span><span class="p">,</span> <span class="s2">&quot;krishpatil1019@gmail.com&quot;</span><span class="p">,</span> <span class="mf">2024</span><span class="p">),</span>
    <span class="k">new</span> <span class="nx">Person</span><span class="p">(</span><span class="s2">&quot;Don Tran&quot;</span><span class="p">,</span> <span class="s2">&quot;donqt15@gmail.com&quot;</span><span class="p">,</span> <span class="mf">2024</span><span class="p">),</span>
    <span class="k">new</span> <span class="nx">Person</span><span class="p">(</span><span class="s2">&quot;Nathan Manangan&quot;</span><span class="p">,</span> <span class="s2">&quot;prorichyman@gmail.com&quot;</span><span class="p">,</span> <span class="mf">2024</span><span class="p">),</span>
    <span class="k">new</span> <span class="nx">Person</span><span class="p">(</span><span class="s2">&quot;Nicholas Ramos&quot;</span><span class="p">,</span> <span class="s2">&quot;nicky.jay77@gmail.com&quot;</span><span class="p">,</span> <span class="mf">2024</span><span class="p">),</span>
<span class="p">];</span>


<span class="kd">function</span> <span class="nx">Classroom</span><span class="p">(</span><span class="nx">teacher</span><span class="p">,</span> <span class="nx">students</span><span class="p">){</span> 

    <span class="nx">teacher</span><span class="p">.</span><span class="nx">setRole</span><span class="p">(</span><span class="s2">&quot;Teacher&quot;</span><span class="p">);</span>
    <span class="k">this</span><span class="p">.</span><span class="nx">teacher</span> <span class="o">=</span> <span class="nx">teacher</span><span class="p">;</span>
    <span class="k">this</span><span class="p">.</span><span class="nx">classroom</span> <span class="o">=</span> <span class="p">[</span><span class="nx">teacher</span><span class="p">];</span>

    <span class="k">this</span><span class="p">.</span><span class="nx">students</span> <span class="o">=</span> <span class="nx">students</span><span class="p">;</span>
    <span class="k">this</span><span class="p">.</span><span class="nx">students</span><span class="p">.</span><span class="nx">forEach</span><span class="p">(</span><span class="nx">student</span> <span class="p">=&gt;</span> <span class="p">{</span> <span class="nx">student</span><span class="p">.</span><span class="nx">setRole</span><span class="p">(</span><span class="s2">&quot;Student&quot;</span><span class="p">);</span> <span class="k">this</span><span class="p">.</span><span class="nx">classroom</span><span class="p">.</span><span class="nx">push</span><span class="p">(</span><span class="nx">student</span><span class="p">);</span> <span class="p">});</span>

    <span class="k">this</span><span class="p">.</span><span class="nx">json</span> <span class="o">=</span> <span class="p">[];</span>
    <span class="k">this</span><span class="p">.</span><span class="nx">classroom</span><span class="p">.</span><span class="nx">forEach</span><span class="p">(</span><span class="nx">person</span> <span class="p">=&gt;</span> <span class="k">this</span><span class="p">.</span><span class="nx">json</span><span class="p">.</span><span class="nx">push</span><span class="p">(</span><span class="nx">person</span><span class="p">.</span><span class="nx">toJSON</span><span class="p">()));</span>
<span class="p">}</span>


<span class="nx">compsci</span> <span class="o">=</span> <span class="k">new</span> <span class="nx">Classroom</span><span class="p">(</span><span class="nx">teacher</span><span class="p">,</span> <span class="nx">students</span><span class="p">);</span>


<span class="nx">logItType</span><span class="p">(</span><span class="nx">compsci</span><span class="p">.</span><span class="nx">classroom</span><span class="p">);</span>  
<span class="nx">logItType</span><span class="p">(</span><span class="nx">compsci</span><span class="p">.</span><span class="nx">classroom</span><span class="p">[</span><span class="mf">0</span><span class="p">].</span><span class="nx">name</span><span class="p">);</span>  
<span class="nx">logItType</span><span class="p">(</span><span class="nx">compsci</span><span class="p">.</span><span class="nx">json</span><span class="p">[</span><span class="mf">0</span><span class="p">]);</span>  
<span class="nx">logItType</span><span class="p">(</span><span class="nx">JSON</span><span class="p">.</span><span class="nx">parse</span><span class="p">(</span><span class="nx">compsci</span><span class="p">.</span><span class="nx">json</span><span class="p">[</span><span class="mf">0</span><span class="p">]));</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">

<div class="output_area">

<div class="output_subarea output_stream output_stdout output_text">
<pre>object ; [ Person {
    name: &#39;Mr M&#39;,
    email: &#39;jmortensen@powayusd.com&#39;,
    classOf: 1977,
    role: &#39;Teacher&#39; },
  Person {
    name: &#39;Krish Patil&#39;,
    email: &#39;krishpatil1019@gmail.com&#39;,
    classOf: 2024,
    role: &#39;Student&#39; },
  Person {
    name: &#39;Don Tran&#39;,
    email: &#39;donqt15@gmail.com&#39;,
    classOf: 2024,
    role: &#39;Student&#39; },
  Person {
    name: &#39;Nathan Manango&#39;,
    email: &#39;prorichyman@gmail.com&#39;,
    classOf: 2024,
    role: &#39;Student&#39; },
  Person {
    name: &#39;Nicholas Ramos&#39;,
    email: &#39;unknown&#39;,
    classOf: 2024,
    role: &#39;Student&#39; } ]
string ; Mr M
string ; {&#34;name&#34;:&#34;Mr M&#34;,&#34;ghID&#34;:&#34;jmortensen@powayusd.com&#34;,&#34;classOf&#34;:1977,&#34;role&#34;:&#34;Teacher&#34;}
object ; { name: &#39;Mr M&#39;,
  ghID: &#39;jmortensen@powayusd.com&#39;,
  classOf: 1977,
  role: &#39;Teacher&#39; }
</pre>
</div>
</div>

</div>
</div>

</div>
    {% endraw %}

    {% raw %}
    
<div class="cell border-box-sizing code_cell rendered">
<div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-javascript"><pre><span></span><span class="nx">Classroom</span><span class="p">.</span><span class="nx">prototype</span><span class="p">.</span><span class="nx">_toHtml</span> <span class="o">=</span> <span class="kd">function</span><span class="p">()</span> <span class="p">{</span>
    <span class="kd">var</span> <span class="nx">style</span> <span class="o">=</span> <span class="p">(</span>
      <span class="s2">&quot;display:inline-block;&quot;</span> <span class="o">+</span>
      <span class="s2">&quot;border: 2px solid white;&quot;</span> <span class="o">+</span>
      <span class="s2">&quot;box-shadow: 0.8em 0.4em 0.4em black;&quot;</span>
    <span class="p">);</span>
  
    <span class="kd">var</span> <span class="nx">body</span> <span class="o">=</span> <span class="s2">&quot;&quot;</span><span class="p">;</span>
    
    <span class="nx">body</span> <span class="o">+=</span> <span class="s2">&quot;&lt;tr&gt;&quot;</span><span class="p">;</span>
    <span class="nx">body</span> <span class="o">+=</span> <span class="s2">&quot;&lt;th&gt;&lt;mark&gt;&quot;</span> <span class="o">+</span> <span class="s2">&quot;Name&quot;</span> <span class="o">+</span> <span class="s2">&quot;&lt;/mark&gt;&lt;/th&gt;&quot;</span><span class="p">;</span>
    <span class="nx">body</span> <span class="o">+=</span> <span class="s2">&quot;&lt;th&gt;&lt;mark&gt;&quot;</span> <span class="o">+</span> <span class="s2">&quot;Email&quot;</span> <span class="o">+</span> <span class="s2">&quot;&lt;/mark&gt;&lt;/th&gt;&quot;</span><span class="p">;</span>
    <span class="nx">body</span> <span class="o">+=</span> <span class="s2">&quot;&lt;th&gt;&lt;mark&gt;&quot;</span> <span class="o">+</span> <span class="s2">&quot;Class Of&quot;</span> <span class="o">+</span> <span class="s2">&quot;&lt;/mark&gt;&lt;/th&gt;&quot;</span><span class="p">;</span>
    <span class="nx">body</span> <span class="o">+=</span> <span class="s2">&quot;&lt;th&gt;&lt;mark&gt;&quot;</span> <span class="o">+</span> <span class="s2">&quot;Role&quot;</span> <span class="o">+</span> <span class="s2">&quot;&lt;/mark&gt;&lt;/th&gt;&quot;</span><span class="p">;</span>
    <span class="nx">body</span> <span class="o">+=</span> <span class="s2">&quot;&lt;/tr&gt;&quot;</span><span class="p">;</span>

    <span class="k">for</span> <span class="p">(</span><span class="kd">var</span> <span class="nx">row</span> <span class="k">of</span> <span class="nx">compsci</span><span class="p">.</span><span class="nx">classroom</span><span class="p">)</span> <span class="p">{</span>

      <span class="nx">body</span> <span class="o">+=</span> <span class="s2">&quot;&lt;tr&gt;&quot;</span><span class="p">;</span>

      <span class="nx">body</span> <span class="o">+=</span> <span class="s2">&quot;&lt;td&gt;&quot;</span> <span class="o">+</span> <span class="nx">row</span><span class="p">.</span><span class="nx">name</span> <span class="o">+</span> <span class="s2">&quot;&lt;/td&gt;&quot;</span><span class="p">;</span>
      <span class="nx">body</span> <span class="o">+=</span> <span class="s2">&quot;&lt;td&gt;&quot;</span> <span class="o">+</span> <span class="nx">row</span><span class="p">.</span><span class="nx">email</span> <span class="o">+</span> <span class="s2">&quot;&lt;/td&gt;&quot;</span><span class="p">;</span>
      <span class="nx">body</span> <span class="o">+=</span> <span class="s2">&quot;&lt;td&gt;&quot;</span> <span class="o">+</span> <span class="nx">row</span><span class="p">.</span><span class="nx">classOf</span> <span class="o">+</span> <span class="s2">&quot;&lt;/td&gt;&quot;</span><span class="p">;</span>
      <span class="nx">body</span> <span class="o">+=</span> <span class="s2">&quot;&lt;td&gt;&quot;</span> <span class="o">+</span> <span class="nx">row</span><span class="p">.</span><span class="nx">role</span> <span class="o">+</span> <span class="s2">&quot;&lt;/td&gt;&quot;</span><span class="p">;</span>
      <span class="nx">body</span> <span class="o">+=</span> <span class="s2">&quot;&lt;tr&gt;&quot;</span><span class="p">;</span>
    <span class="p">}</span>
  

    <span class="k">return</span> <span class="p">(</span>
      <span class="s2">&quot;&lt;div style=&#39;&quot;</span> <span class="o">+</span> <span class="nx">style</span> <span class="o">+</span> <span class="s2">&quot;&#39;&gt;&quot;</span> <span class="o">+</span>
        <span class="s2">&quot;&lt;table&gt;&quot;</span> <span class="o">+</span>
          <span class="nx">body</span> <span class="o">+</span>
        <span class="s2">&quot;&lt;/table&gt;&quot;</span> <span class="o">+</span>
      <span class="s2">&quot;&lt;/div&gt;&quot;</span>
    <span class="p">);</span>
  
  <span class="p">};</span>
  

  <span class="nx">$$</span><span class="p">.</span><span class="nx">html</span><span class="p">(</span><span class="nx">compsci</span><span class="p">.</span><span class="nx">_toHtml</span><span class="p">());</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">

<div class="output_area">


<div class="output_html rendered_html output_subarea output_execute_result">
<div style='display:inline-block;border: 2px solid white;box-shadow: 0.8em 0.4em 0.4em black;'><table><tr><th><mark>Name</mark></th><th><mark>Email</mark></th><th><mark>Class Of</mark></th><th><mark>Role</mark></th></tr><tr><td>Mr M</td><td>jmortensen@powayusd.com</td><td>1977</td><td>Teacher</td><tr><tr><td>Krish Patil</td><td>krishpatil1019@gmail.com</td><td>2024</td><td>Student</td><tr><tr><td>Don Tran</td><td>donqt15@gmail.com</td><td>2024</td><td>Student</td><tr><tr><td>Nathan Manango</td><td>prorichyman@gmail.com</td><td>2024</td><td>Student</td><tr><tr><td>Nicholas Ramos</td><td>unknown</td><td>2024</td><td>Student</td><tr></table></div>
</div>

</div>

</div>
</div>

</div>
    {% endraw %}

</div>
 
