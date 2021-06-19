# Reader Mode Testing

I'd like to be able to test various patterns to see how well they appear in reader mode. 

First, what needs to be as Markdown & which as a .html file?

<main>
<article aria-label="headings">
<h1>1 This is 1st level heading</h1>
<p>a This is a test paragraph.</p>
<h2>2 This is 2nd level heading</h2>
<p>a This is a test paragraph.</p>
<h3>3 This is 3rd level heading</h3>
<p>a This is a test paragraph.</p>
<h4>4 This is 4th level heading</h4>
<p>a This is a test paragraph.</p>
<h5>5 This is 5th level heading</h5>
<p>a This is a test paragraph.</p>
<h6>6 This is 6th level heading</h6>
<p>a This is a test paragraph.</p>
</article>

<article>
<h2>7 Basic block level elements</h2>

<p>a This is a normal paragraph (<code>p</code> element).
To add some length to it, let us mention that this page was
primarily written for testing the effect of <strong>user style sheets</strong>.
You can use it for various other purposes as well, like just checking how
your browser displays various HTML elements by default.
It can also be useful when testing conversions from HTML
format to other formats, since some elements can go wrong then.</p>

<p>b This is another paragraph. I think it needs to be added that
the set of elements tested is not exhaustive in any sense. I have selected
those elements for which it can make sense to write user style sheet rules,
in my opionion.</p>

<div>c This is a <code>div</code> element. Authors may use such elements instead
of paragraph markup for various reasons. (End of <code>div</code>.)</div>

<blockquote>
  <p>d This is a block quotation containing a single
paragraph. Well, not quite, since this is not <em>really</em>
quoted text, but I hope you understand the point. After all, this
page does not use HTML markup very normally anyway.</p>
</blockquote>
<p>e The following contains address information about the author, in an <code>address</code>
element.</p>
<address>
<a href="../somelink.html" lang="fr" hreflang="en">f Mon nom en francais</a>,
<a href="mailto:example@example.com">g example@example.com</a><br>
h 3 Rue Jules Ferry, Neuilly Sur Seine, France 94000
</address></article>


<article>
<h2>8 Lists</h2>

<p>a This is a paragraph before an <strong>unnumbered</strong> list (<code>ul</code>). Note that
the spacing between a paragraph and a list before or after that is hard
to tune in a user style sheet. You can't guess which paragraphs are
logically related to a list, e.g. as a "list header".</p>
<ul>
  <li>b  One.</li>
  <li>c  Two.</li>
  <li>d Three. Well, probably this list item should be longer. Note that
for short items lists look better if they are compactly presented,
       whereas for long items, it would be better to have more vertical spacing between items.</li>
  <li>e Four. This is the last item in this list.
       Let us terminate the list now without making any more fuss about it.</li>
</ul>
<p>f The following is a <code>menu</code> list:</p>
<menu>
  <li>g One.</li>
  <li>h Two.</li>
  <li>i Three. Well, probably this list item should be longer so that it will
probably wrap to the next line in rendering.</li>
</menu>
<p>j The following is a <code>dir</code> list:</p>
<dir>
  <li>k One.</li>
  <li>l Two.</li>
  <li> m Three. Well, probably this list item should be longer so that it will
probably wrap to the next line in rendering.</li>
</dir>

<p>n This is a paragraph before a <strong>numbered</strong> list (<code>ol</code>). Note that
the spacing between a paragraph and a list before or after that is hard
to tune in a user style sheet. You can't guess which paragraphs are
logically related to a list, e.g. as a "list header".</p>
<ol>
  <li>o One.</li>
  <li>p Two.</li>
  <li>q Three. Well, probably this list item should be longer. Note that if
items are short, lists look better if they are compactly presented,
       whereas for long items, it would be better to have more vertical spacing between items.</li>
  <li>r Four. This is the last item in this list.
       Let us terminate the list now without making any more fuss about it.</li>
</ol>

<p>s This is a paragraph before a <strong>definition</strong> list (<code>dl</code>).
In principle, such a list should consist of <em>terms</em> and associated 
definitions.
But many authors use <code>dl</code> elements for fancy "layout" things. Usually the
effect is not <em>too</em> bad, if you design user style sheet rules for <code>dl</code>
which are suitable
for real definition lists.</p>
<dl>
  <dt>t recursion</dt>
  <dd>u see recursion</dd>
  <dt>v recursion, indirect</dt>
  <dd>w see indirect recursion</dd>
  <dt>x indirect recursion</dt>
  <dd>y see recursion, indirect</dd>
  <dt>z term</dt>
  <dd>aa a word or other expression taken into specific use in
       a well-defined meaning, which is often defined rather rigorously, even
       formally, and may differ quite a lot from an everyday meaning</dd>
</dl>
</article>

<article>
<h2>9 Text-level markup, in alphabetical order</h2>

<ul>
  <li>a <abbr title="Cascading Style Sheets">CSS</abbr> (an abbreviation;
 <code>abbr</code> markup used)</li>
  <li>b <acronym title="radio detecting and ranging">radar</acronym> (an acronym; <code>acronym</code> markup used)</li>
  <li>c <b>bolded</b> (<code>b</code> markup used - just bolding with unspecified
       semantics)</li>
  <li>d <cite>Origin of Species</cite> (a book title;
       <code>cite</code> markup used)</li>
  <li>e <code>a[i] = b[i] + c[i);</code> (computer code; <code>code</code> markup used)</li>
  <li>f here we have some <del>deleted</del> text (<code>del</code> markup used)</li>
  <li>g an <dfn>octet</dfn> is an entity consisting of eight bits
       (<code>dfn</code> markup used for the term being defined)</li>
  <li>h this is <em>very</em> simple (<code>em</code> markup used for emphasizing
       a word)</li>
  <li>i <i lang="la">Homo sapiens</i> (should appear in italics;  <code>i</code> markup used)</li>
  <li>j here we have some <ins>inserted</ins> text (<code>ins</code> markup used)</li>
  <li>k type <kbd>yes</kbd> when prompted for an answer (<code>kbd</code> markup
       used for text indicating keyboard input)</li>
  <li>l <q>Hello!</q> (<code>q</code> markup used for quotation)</li>
  <li>m He said: <q>She said <q>Hello!</q></q> (a quotation inside a quotation)</li>
  <li>n you may get the message <samp>Core dumped</samp> at times
       (<code>samp</code> markup used for sample output)</li>
  <li>o <small>this is not that important</small> (<code>small</code> markup used)</li>
  <li>p <strike>overstruck</strike> (<code>strike</code> markup used; note:
       <code>s</code> is a nonstandard synonym for <code>strike</code>)</li>
  <li>q <strong>this is highlighted text</strong> (<code>strong</code>
       markup used)</li>
  <li>r In order to test how subscripts and superscripts (<code>sub</code> and
       <code>sup</code> markup) work inside running text, we need some
       dummy text around constructs like x<sub>1</sub> and H<sub>2</sub>O
       (where subscripts occur). So here is some fill so that
       you will (hopefully) see whether and how badly the subscripts
       and superscripts mess up vertical spacing between lines.
       Now superscripts: M<sup>lle</sup>, 1<sup>st</sup>, and then some
       mathematical notations: e<sup>x</sup>, sin<sup>2</sup> <i>x</i>,
       and some nested superscripts (exponents) too:
       e<sup>x<sup>2</sup></sup> and f(x)<sup>g(x)<sup>a+b+c</sup></sup>
       (where 2 and a+b+c should appear as exponents of exponents).</li>
  <li>s <tt>text in monospace font</tt> (<code>tt</code> markup used)</li>
  <li>t <u>underlined</u> text (<code>u</code> markup used)</li>
  <li>u the command <code>cat</code> <var>filename</var> displays the
       file specified by the <var>filename</var> (<code>var</code> markup
       used to indicate a word as a variable).</li>
</ul>

<p>v Some of the elements tested above are typically displayed in a monospace
font, often using the <em>same</em> presentation for all of them. This
tests whether that is the case on your browser:</p>

<ul>
  <li>w <code>This is sample text inside code markup</code></li>
  <li>x <kbd>This is sample text inside kbd markup</kbd></li>
  <li>y <samp>This is sample text inside samp markup</samp></li>
  <li>z <tt>This is sample text inside tt markup</tt></li>
</ul>
  
<h2>10 Links</h2>
<ul>
<li>a <a href="../index.html">main page</a></li>
<li>b <a href=
"http://www.unicode.org/versions/Unicode4.0.0/ch06.pdf"
title="Writing Systems and Punctuation"
type="application/pdf"
>Unicode Standard, chapter&nbsp;6</a></li>
</ul>

<p>c This is a text paragraph that contains some
inline links. Generally, inline links (as opposite to e.g. links
lists) are problematic
from the
<a href="http://www.useit.com">usability</a> perspective,
but they may have use as
&#8220;incidental&#8221;, less relevant links. See the document
<cite><a href="links.html">d Links Want To Be Links</a></cite>.</p>
</article>


<article>
<h2>11 Forms</h2>

<form action="somewhere.cgi">
<div>
<input type="hidden" name="hidden field" value="42"/>
a This is a form containing various fields (with some initial
values (defaults) set, so that you can see how input text looks
like without actually typing it):</div>
    <ul>
        <li><label for="zname">b Name</label><input type="text" class="classed" required="" placeholder=" Name" id="zname"></li>
        <li><label for="zemail">c Email</label><input type="email" class="classed" multiple="" placeholder="email addresses" required="" id="zemail"></li>
        <li><label for="zdob">d Birthday</label><input type="date" class="classed" required="" placeholder="01/01/84" id="zdob"></li>
        <li><label for="zage">e Age</label><input type="number" class="classed" required="" min="21" max="105" id="zage"></li>
        <li><label for="zphone">f Phone</label><input type="tel" class="classed" pattern="\d{3}-\d{3}-\d{4}" placeholder="XXX-XXX-XXXX" id="zphone"></li>
        <li><label for="zrange">g Satisfaction</label><input type="range" id="zrange" min="0" max="10" step="1" list="zrangelist">

          <datalist id="zrangelist">
            <option value="7">h 7</option>
            <option value="8">i 8</option>
            <option value="9">j 9</option>
            <option value="10">k 10</option>
          </datalist>
        </li><li><label for="ztweet">l Twitter</label><input type="text" class="classed" pattern="@\w*" placeholder="@twitter" required="" id="ztweet"></li>
        <li>
        <input type="submit" value="m submit"></li>
                        </ul>

<div><label for="but">n Button:
<button id="but" type="submit" name="foo" value="bar">A cool<br>button</button></label></div>

<div><label for="f0">o Reset button:
<input id="f0" type="reset" name="reset" value="Reset"></label></div>

<div><label for="f1">p Single-line text input field: <input id="f1" name="text" size="20" value="Default text."></label></div>

<div><label for="f2">q Multi-line text input field (textarea):</label><br>
<textarea id="f2" name="textarea" rows="2" cols="20">
r Default text.
</textarea></div>

<div>s The following two radio buttons are inside
a <code>fieldset</code> element with a <code>legend</code>:</div>

<fieldset>
<legend>t Legend</legend>
<div><label for="f3"><input id="f3" type="radio" name="radio" value="1">u Radio button 1</label></div>
<div><label for="f4"><input id="f4" type="radio" name="radio" value="2" checked>v Radio button 2 (initially checked)</label></div>
</fieldset>

<fieldset>
<legend>w Check those that apply</legend>
<div><label for="f5"><input id="f5" type="checkbox" name="checkbox">x Checkbox 1</label></div>
<div><label for="f6"><input id="f6" type="checkbox" name="checkbox2" checked>y Checkbox 2 (initially checked)</label></div>
</fieldset>

<div><label for="f10">A <code>select</code>z element with <code>size="1"</code>
(dropdown box):
<select id="f10" name="select1" size="1">
<option>aa one</option>
<option selected>bb two (default)</option>
<option>cc three</option>
</select></label></div>

<div><label for="f11">dd A <code>select</code> element with <code>size="3"</code>
(listbox):</label><br>
<select id="f11" name="select2" size="3">
<option>ee one</option>
<option selected>ff two (default)</option>
<option>gg three</option>
</select></div>
<div><label for="f99">hh Submit button:
<input id="f99" type="submit" name="submit" value="Just a test"></label></div>
</form>
</article>

<article>
<h2>12 Tables</h2>

<p>a The following table has a caption. The first row is in a thead, the second row is the tfoot, and the rest is in a tbody. The first column
contain table header cells (<code>th</code> elements) only; other cells
are data cells (<code>td</code> elements):</p>

<table summary=
"Each row names a Nordic country and specifies its total area and land area, in square kilometers">
<caption>Sample table: Areas of the Nordic countries, in sq km</caption>
<thead><tr><th scope="col">b Country</th> <th scope="col">c Total area</th> <th scope="col">d Land area</th></tr></thead>
<tbody>
<tr><th scope="row">e Denmark</th> <td>f 43,070 </td><td>g 42,370</td></tr>
<tr><th scope="row">h Finland</th> <td>i 337,030 </td><td>j 305,470</td></tr>
<tr><th scope="row">k Iceland</th> <td>l 103,000 </td><td>m 100,250</td></tr>
<tr><th scope="row">n Norway</th>  <td>o 324,220 </td><td>p 307,860</td></tr>
<tr><th scope="row">q Sweden</th>  <td>r 449,964 </td><td>s 410,928</td></tr>
</tbody>
<tfoot><tr><th scope="col">Country</th> <th scope="col">Total area</th> <th scope="col">t Land area</th></tr></tfoot>
</table>
</article>


<article>
<h2>13 HTML5 Elements</h2>

<h3>a Details and Summary</h3>
<details>
  <summary>b This is the summary of the details</summary>
  <p>c This is a paragraph within a <code>details</code> element, outside of the <code>summary</code></p>
</details>

<h3>d Figure and Figcaption</h3>
<figure>
  <img src="none.jpg" alt="img with invalid src">
  <figcaption>e This is the figcaption
  </figcaption>
</figure>

<dialog>f This is a dialog</dialog>

<p>g This paragraph has a <mark>mark</mark></p>

<h3>h Meter</h3>
<ul>
<li><meter>i Meter</meter></li>
<li><meter value=1 min=0 max=4 low=2 high=3>j 1 of 4</meter></li>
<li><meter value=2 min=0 max=4 low=1 high=3>k 2 of 4</meter></li>
<li><meter value=61 min=0 max=100 low=73 high=87 optimum=100>l 1</meter></li>
</ul>
<h3>m Progress</h3>
<ul>
<li><progress>n Empty</progress></li>
<li><progress min="0" max="100" value="17">o 17% complete</progress></li>
<li><progress value="75" max="100">p 75% complete</progress></li>
</ul>

</article>

<aside>
<h1>14 This is an aside</h1>
<h2>a Character test</h2>
<p>b The following table has some sample characters with
annotations. If the browser&#8217;s default font does not
contain all of them, they may get displayed using backup fonts.
This may cause stylistic differences, but it should not
prevent the characters from being displayed at all.</p>

<table>
<thead><tr><th>c Char.</th> <th>d Explanation </th> <th>e Notes</th></tr></thead>
<tbody><tr><td>f ê </td><td>g e with circumflex </td><td>h Latin 1 character, should be ok</td></tr>
<tr><td>i &#8212;</td> <td>j em dash </td><td>k Windows Latin 1 character, should be ok, too</td></tr>
<tr><td>l &#x100;</td> <td>m A with macron (line above) </td><td>n Latin Extended-A character, not present in all fonts</td></tr>
<tr><td>o &Omega;</td> <td>p capital omega </td><td>q A Greek letter</td></tr>
<tr><td>r &#x2212;</td> <td>s minus sign </td><td>t Unicode minus</td></tr>
<tr><td>u &#x2300;</td> <td>v diameter sign </td><td>w relatively rare in fonts</td></tr>
</tbody>
</table>
</aside>
</main>

<footer>
<hr title="Information about this document"/>
<p>x This <code>footer</code> starts with an <code>hr</code>, followed by two <code>p</code>s.</p>
<p>y Last update: <time>2019-06-22</time>.</p>
</footer>



Thanks to 
- https://github.com/estelle/html_elements
