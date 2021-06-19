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

Gotta add more text, so why not Amanda Gorman poem from the inauguration of President Joe Biden on January 20:
            
<p class="zn-body__paragraph speakable" data-paragraph-id="paragraph_9F856194-1405-FA24-EBAB-222930E70404" data-act-id="paragraph_0"><cite class="el-editorial-source"> (CNN)</cite>Amanda Gorman, the nation's <a href="https://www.cnn.com/2021/01/20/politics/amanda-gorman-inauguration-poem-trnd/index.html" target="_blank">first-ever youth poet laureate</a>, read the following poem during the <a href="https://www.cnn.com/politics/live-news/biden-harris-inauguration-day-2021/index.html" target="_blank">inauguration of President Joe Biden</a> on January 20:</p></div><div class="zn-body__paragraph" data-paragraph-id="paragraph_78E4E2C5-3666-92A7-BCB8-222110D1A624" data-act-id="paragraph_1">When day comes we ask ourselves,</div><div class="zn-body__paragraph" data-paragraph-id="paragraph_0D4EDE91-B5C8-4FF0-63A5-222222F391C8" data-act-id="paragraph_2">where can we find light in this never-ending shade?</div><div class="ad ad--epic ad--mobile" data-ad-text="show"><div data-ad-id="ad_nat_btf_01" data-ad-position="mobile" data-ad-refresh="default"></div></div><ul class="cn cn-list-hierarchical-xs cn--idx-4 cn-zoneAdContainer" data-layout="list-hierarchical-xs"></ul><div class="zn-body__paragraph" data-paragraph-id="paragraph_A5413C53-03AD-3B53-3450-222222F46E7B" data-act-id="paragraph_3">The loss we carry,</div><div class="ad ad--epic ad--tablet" data-ad-text="show"><div data-ad-id="ad_nat_btf_01" data-ad-position="tablet" data-ad-refresh="default"></div></div><div class="ad ad--epic ad--desktop" data-ad-text="show"><div data-ad-id="ad_nat_btf_01" data-ad-position="desktop" data-ad-refresh="default"><div id="ad_nat_btf_01" class="ad-ad_nat_btf_01 ad-refresh-default"></div></div></div><ul class="cn cn-list-hierarchical-xs cn--idx-6 cn-zoneAdContainer" data-layout="list-hierarchical-xs"></ul><div class="zn-body__paragraph" data-paragraph-id="paragraph_57D799F8-BBA6-7661-47BB-222222F6A13C" data-act-id="paragraph_4">a sea we must wade</div><div class="ad ad--epic ad--mobile" data-ad-text="show"><div data-ad-id="ad_rect_atf_01" data-ad-position="mobile" data-ad-refresh="default"></div></div><ul class="cn cn-list-hierarchical-xs cn--idx-8 cn-zoneAdContainer" data-layout="list-hierarchical-xs"></ul><div class="zn-body__read-more"><div class="read-more-gradient"></div><div class="read-more-button" data-zjs="click" data-zjs-campaign="readmore-btn-mobile"><div class="read-more-link" id="js-body-read-more">Read More</div></div></div><div class="zn-body__read-all"><div class="zn-body__paragraph" data-paragraph-id="paragraph_A581C01D-4A6B-DB7B-F020-222222F786F0" data-act-id="paragraph_5">We've braved the belly of the beast</div><div class="zn-body__paragraph" data-paragraph-id="paragraph_372AFA3C-C551-25D5-2BB8-222222FAB0ED" data-act-id="paragraph_6">We've learned that quiet isn't always peace</div><div class="ad ad--epic ad--mobile" data-ad-text="show"><div data-ad-id="ad_rect_atf_02" data-ad-position="mobile" data-ad-refresh="default"></div></div><ul class="cn cn-list-hierarchical-xs cn--idx-12 cn-zoneAdContainer" data-layout="list-hierarchical-xs"></ul><div class="zn-body__paragraph" data-paragraph-id="paragraph_098DB461-7C6D-AC17-0887-222222FCC532" data-act-id="paragraph_7">And the norms and notions</div><div class="zn-body__paragraph" data-paragraph-id="paragraph_CA7C4F1A-C6C7-3E0B-C0A9-222222FE2EB2" data-act-id="paragraph_8">of what just is</div><div class="zn-body__paragraph" data-paragraph-id="paragraph_5C5E69C4-486C-FF69-9208-222222FF172F" data-act-id="paragraph_9">Isn't always just-ice</div><div class="zn-body__paragraph" data-paragraph-id="paragraph_B3C45016-99FF-A589-EC91-22222301F4D2" data-act-id="paragraph_10">And yet the dawn is ours</div><div class="zn-body__paragraph" data-paragraph-id="paragraph_BBA0488C-18F5-4E56-4B1E-222223039898" data-act-id="paragraph_11">before we knew it</div><div class="zn-body__paragraph" data-paragraph-id="paragraph_9C46BD6F-0410-B89A-8082-222223042846" data-act-id="paragraph_12">Somehow we do it</div><div class="zn-body__paragraph" data-paragraph-id="paragraph_B88AEC72-F691-BA0E-B228-2222230532FB" data-act-id="paragraph_13">Somehow we've weathered and witnessed</div><div class="zn-body__paragraph" data-paragraph-id="paragraph_1E153687-DE71-19F5-54D6-22222307CF24" data-act-id="paragraph_14">a nation that isn't broken</div><div class="zn-body__paragraph" data-paragraph-id="paragraph_227F0C8B-57CB-D52C-81B1-222223094CD9" data-act-id="paragraph_15">but simply unfinished</div><div class="zn-body__paragraph" data-paragraph-id="paragraph_E050AC32-751B-171E-C78F-2222230A3C21" data-act-id="paragraph_16">We the successors of a country and a time</div><div class="zn-body__paragraph" data-paragraph-id="paragraph_38CB9928-BEE3-C0F7-9E48-2222230C9A1E" data-act-id="paragraph_17">Where a skinny Black girl</div><div class="zn-body__paragraph" data-paragraph-id="paragraph_5649B3F4-36D6-4DDA-D60A-2222230EEB93" data-act-id="paragraph_18">descended from slaves and raised by a single mother</div><div class="zn-body__paragraph" data-paragraph-id="paragraph_8D00A4CF-1847-9F73-578C-222223114CC0" data-act-id="paragraph_19">can dream of becoming president</div><div class="zn-body__paragraph" data-paragraph-id="paragraph_DC87C641-C82D-E272-AA09-22222313278E" data-act-id="paragraph_20">only to find herself reciting for one</div><div class="zn-body__paragraph" data-paragraph-id="paragraph_65C0AFAD-7355-ECCB-8840-222223158EB8" data-act-id="paragraph_21">And yes we are far from polished</div><div class="zn-body__paragraph" data-paragraph-id="paragraph_CC5B3D93-68D8-C4D7-BA6C-22222316F1C6" data-act-id="paragraph_22">far from pristine</div><div class="zn-body__paragraph" data-paragraph-id="paragraph_2F3E42D6-1F84-E43C-6093-2222231810B0" data-act-id="paragraph_23">but that doesn't mean we are</div><div class="zn-body__paragraph" data-paragraph-id="paragraph_5E1D9E48-62CC-F78E-3310-2222231AC1F9" data-act-id="paragraph_24">striving to form a union that is perfect</div><div class="zn-body__paragraph" data-paragraph-id="paragraph_F5FEA26E-E42A-BBB8-CF46-2222231D8C4D" data-act-id="paragraph_25">We are striving to forge a union with purpose</div><div class="zn-body__paragraph" data-paragraph-id="paragraph_470ECE2E-01D3-3291-171F-2222231F90D7" data-act-id="paragraph_26">To compose a country committed to all cultures, colors, characters and</div><div class="zn-body__paragraph" data-paragraph-id="paragraph_44A9D0ED-2AA9-CF57-641A-22222321BD66" data-act-id="paragraph_27">conditions of man</div><div class="zn-body__paragraph" data-paragraph-id="paragraph_76A8AFC6-08BF-F337-5198-22222323E9C6" data-act-id="paragraph_28">And so we lift our gazes not to what stands between us</div><div class="zn-body__paragraph" data-paragraph-id="paragraph_1E624FF0-CCD4-2177-A6F5-22222326BD87" data-act-id="paragraph_29">but what stands before us</div><div class="zn-body__paragraph" data-paragraph-id="paragraph_D7DB52C6-9C9C-95DD-7B76-2222232873F7" data-act-id="paragraph_30">We close the divide because we know, to put our future first,</div><div class="zn-body__paragraph" data-paragraph-id="paragraph_684F8B43-E404-DBE9-F0AD-2222232B785E" data-act-id="paragraph_31">we must first put our differences aside</div><div class="zn-body__paragraph" data-paragraph-id="paragraph_6E479CF4-5602-F6C9-B52A-2222232D9F6E" data-act-id="paragraph_32">We lay down our arms</div><div class="zn-body__paragraph" data-paragraph-id="paragraph_CED8E67E-DFFA-2947-E0EE-2222233066AE" data-act-id="paragraph_33">so we can reach out our arms</div><div class="zn-body__paragraph" data-paragraph-id="paragraph_32B1E988-E3E1-D21A-C990-222223332044" data-act-id="paragraph_34">to one another</div><div class="zn-body__paragraph" data-paragraph-id="paragraph_51483B67-0EE4-A363-6398-222223379A93" data-act-id="paragraph_35">We seek harm to none and harmony for all</div><div class="zn-body__paragraph" data-paragraph-id="paragraph_31EA3241-0C4C-98C6-3DF3-2222233A3614" data-act-id="paragraph_36">Let the globe, if nothing else, say this is true:</div><div class="zn-body__paragraph" data-paragraph-id="paragraph_2E1B32CF-582B-E860-59C1-2222233C14A4" data-act-id="paragraph_37">That even as we grieved, we grew</div><div class="zn-body__paragraph" data-paragraph-id="paragraph_1B154248-3E88-B697-4E64-2222233FF898" data-act-id="paragraph_38">That even as we hurt, we hoped</div><div class="zn-body__paragraph" data-paragraph-id="paragraph_A8D1382F-5EA8-B4DF-B5E2-222223421B31" data-act-id="paragraph_39">That even as we tired, we tried</div><div class="zn-body__paragraph" data-paragraph-id="paragraph_AC3A7BF0-9F7C-6EE4-9138-22222346B386" data-act-id="paragraph_40">That we'll forever be tied together, victorious</div><div class="zn-body__paragraph" data-paragraph-id="paragraph_6BE5D2BA-26F1-AA78-E072-2222234938AC" data-act-id="paragraph_41">Not because we will never again know defeat</div><div class="zn-body__paragraph" data-paragraph-id="paragraph_7CC7E993-E751-F12C-9A3B-2222234C4FA2" data-act-id="paragraph_42">but because we will never again sow division</div><div class="zn-body__paragraph" data-paragraph-id="paragraph_809B6849-7234-26C0-5F80-2222234F85D4" data-act-id="paragraph_43">Scripture tells us to envision</div><div class="zn-body__paragraph" data-paragraph-id="paragraph_0EAEC649-C9B4-86D1-05EF-222223537A6C" data-act-id="paragraph_44">that everyone shall sit under their own vine and fig tree</div><div class="zn-body__paragraph" data-paragraph-id="paragraph_049FE5DF-7131-C093-F922-222223563F94" data-act-id="paragraph_45">And no one shall make them afraid</div><div class="zn-body__paragraph" data-paragraph-id="paragraph_F5FB5A48-5654-48EC-D546-2222235A3BB0" data-act-id="paragraph_46">If we're to live up to our own time</div><div class="zn-body__paragraph" data-paragraph-id="paragraph_07F200BF-DD05-4F10-5DE0-2222235DCF99" data-act-id="paragraph_47">Then victory won't lie in the blade</div><div class="zn-body__paragraph" data-paragraph-id="paragraph_BB7ED2F9-64B1-8C3B-D5F5-222223600F6C" data-act-id="paragraph_48">But in all the bridges we've made</div><div class="zn-body__paragraph" data-paragraph-id="paragraph_029A9683-BC0D-62B8-4422-22222364667A" data-act-id="paragraph_49">That is the promise to glade</div><div class="zn-body__paragraph" data-paragraph-id="paragraph_1066ECBE-CFE7-FCEA-1081-222223676F81" data-act-id="paragraph_50">The hill we climb</div><div class="zn-body__paragraph" data-paragraph-id="paragraph_C4E525EE-6681-DDB5-AC3B-2222236BA1F3" data-act-id="paragraph_51">If only we dare</div><div class="zn-body__paragraph" data-paragraph-id="paragraph_2714B674-1DB0-E84C-90AD-2222236F26CF" data-act-id="paragraph_52">It's because being American is more than a pride we inherit,</div><div class="zn-body__paragraph" data-paragraph-id="paragraph_2EB4F94B-0422-CF76-F9B9-22222374FA4B" data-act-id="paragraph_53">it's the past we step into</div><div class="zn-body__paragraph" data-paragraph-id="paragraph_B6D05AF2-F623-D298-87DE-22222378FBA8" data-act-id="paragraph_54">and how we repair it</div><div class="zn-body__paragraph" data-paragraph-id="paragraph_6143FC3B-BA45-E57F-F210-2222237CA07E" data-act-id="paragraph_55">We've seen a force that would shatter our nation</div><div class="zn-body__paragraph" data-paragraph-id="paragraph_302F786A-298D-2A3A-8E49-2222238026EF" data-act-id="paragraph_56">rather than share it</div><div class="zn-body__paragraph" data-paragraph-id="paragraph_500AC650-F5AF-3F40-674D-222223859601" data-act-id="paragraph_57">Would destroy our country if it meant delaying democracy</div><div class="zn-body__paragraph" data-paragraph-id="paragraph_83972C60-73E5-D03D-BCF5-2222238B7698" data-act-id="paragraph_58">And this effort very nearly succeeded</div><div class="zn-body__paragraph" data-paragraph-id="paragraph_2FFD7351-CFEB-2D6F-CAF1-2222238FE8F9" data-act-id="paragraph_59">But while democracy can be periodically delayed</div><div class="zn-body__paragraph" data-paragraph-id="paragraph_2912679A-AC2D-FA97-9F93-222223A74E64" data-act-id="paragraph_60">it can never be permanently defeated</div><div class="zn-body__paragraph" data-paragraph-id="paragraph_6CC90B00-2C6C-36A3-F11A-222223AC7EC4" data-act-id="paragraph_61">In this truth</div><div class="zn-body__paragraph" data-paragraph-id="paragraph_A0BB6011-0FFA-540A-6145-222223B24783" data-act-id="paragraph_62">in this faith we trust</div><div class="zn-body__paragraph" data-paragraph-id="paragraph_BF036934-0139-6E3E-90F2-222223BD8FB7" data-act-id="paragraph_63">For while we have our eyes on the future</div><div class="zn-body__paragraph" data-paragraph-id="paragraph_C31177D6-F3A2-A6BC-4054-222223C3D0A5" data-act-id="paragraph_64">history has its eyes on us</div><div class="zn-body__paragraph" data-paragraph-id="paragraph_98B24D54-3C53-1EF4-1064-222223CD8501" data-act-id="paragraph_65">This is the era of just redemption</div><div class="zn-body__paragraph" data-paragraph-id="paragraph_3460EAF3-1079-0214-8322-222223D2DFD9" data-act-id="paragraph_66">We feared at its inception</div><div class="zn-body__paragraph" data-paragraph-id="paragraph_676B3DA7-6E10-ABE9-2DE7-222223DD9C52" data-act-id="paragraph_67">We did not feel prepared to be the heirs</div><div class="zn-body__paragraph" data-paragraph-id="paragraph_24473C4C-005C-D116-E042-222223E3FB26" data-act-id="paragraph_68">of such a terrifying hour</div><div class="zn-body__paragraph" data-paragraph-id="paragraph_2DD40ABB-857F-04C2-2B09-222223ED1768" data-act-id="paragraph_69">but within it we found the power</div><div class="zn-body__paragraph" data-paragraph-id="paragraph_5B4F0F9F-9E7C-6F29-77CF-222223F54ABA" data-act-id="paragraph_70">to author a new chapter</div><div class="zn-body__paragraph" data-paragraph-id="paragraph_B78E530A-9E65-70E5-9AD4-222224025623" data-act-id="paragraph_71">To offer hope and laughter to ourselves</div><div class="zn-body__paragraph" data-paragraph-id="paragraph_5876F57D-AD6B-AEBB-F7F3-2222240BD4A4" data-act-id="paragraph_72">So while once we asked,</div><div class="zn-body__paragraph" data-paragraph-id="paragraph_BE1D2B3D-46DE-BBCC-3753-22222418D686" data-act-id="paragraph_73">how could we possibly prevail over catastrophe?</div><div class="zn-body__paragraph" data-paragraph-id="paragraph_3943F9F5-5DEA-F99E-C8A9-2222241F76DD" data-act-id="paragraph_74">Now we assert</div><div class="zn-body__paragraph" data-paragraph-id="paragraph_34168606-ADB7-D748-6D50-2222242EADF8" data-act-id="paragraph_75">How could catastrophe possibly prevail over us?</div><div class="zn-body__paragraph" data-paragraph-id="paragraph_FCBF874B-BCB6-EA90-88D6-22222436979D" data-act-id="paragraph_76">We will not march back to what was</div><div class="zn-body__paragraph" data-paragraph-id="paragraph_16EC7096-B839-BD74-570B-2222243E058D" data-act-id="paragraph_77">but move to what shall be</div><div class="zn-body__paragraph" data-paragraph-id="paragraph_9D07F42B-A934-4758-F5E2-2222244A741F" data-act-id="paragraph_78">A country that is bruised but whole,</div><div class="zn-body__paragraph" data-paragraph-id="paragraph_15F23BAC-C470-8327-5703-222224530E02" data-act-id="paragraph_79">benevolent but bold,</div><div class="zn-body__paragraph" data-paragraph-id="paragraph_A5E71E4C-367E-2E1E-604F-2222245FE8C7" data-act-id="paragraph_80">fierce and free</div><div class="zn-body__paragraph" data-paragraph-id="paragraph_932B51C7-F393-58C0-BA43-22222467D569" data-act-id="paragraph_81">We will not be turned around</div><div class="zn-body__paragraph" data-paragraph-id="paragraph_66D9AAFF-54C7-54FA-DBAD-222224762062" data-act-id="paragraph_82">or interrupted by intimidation</div><div class="zn-body__paragraph" data-paragraph-id="paragraph_27041768-AFB5-D1D8-3C52-22222487AD34" data-act-id="paragraph_83">because we know our inaction and inertia</div><div class="zn-body__paragraph" data-paragraph-id="paragraph_E04F829F-7F80-B93E-B175-22222498F2D2" data-act-id="paragraph_84">will be the inheritance of the next generation</div><div class="zn-body__paragraph" data-paragraph-id="paragraph_8AEC23E0-D07E-485A-7893-222224A5A899" data-act-id="paragraph_85">Our blunders become their burdens</div><div class="zn-body__paragraph" data-paragraph-id="paragraph_ECC7DC86-4FA5-DF68-53EB-222224B6C00B" data-act-id="paragraph_86">But one thing is certain:</div><div class="zn-body__paragraph" data-paragraph-id="paragraph_77CFD409-2528-A533-018C-222224C08968" data-act-id="paragraph_87">If we merge mercy with might,</div><div class="zn-body__paragraph" data-paragraph-id="paragraph_01497EC5-FE05-5143-5E39-222224D4B88D" data-act-id="paragraph_88">and might with right,</div><div class="zn-body__paragraph" data-paragraph-id="paragraph_F58F138F-DDCE-826E-5C4A-222224E0B770" data-act-id="paragraph_89">then love becomes our legacy</div><div class="zn-body__paragraph" data-paragraph-id="paragraph_81022F06-D671-C93B-234E-222224F471C1" data-act-id="paragraph_90">and change our children's birthright</div><div class="zn-body__paragraph" data-paragraph-id="paragraph_C4E2804B-DD61-5786-8840-222224FE0B80" data-act-id="paragraph_91">So let us leave behind a country</div><div class="zn-body__paragraph" data-paragraph-id="paragraph_EA87D1B9-C915-75B1-30C4-2222250C732A" data-act-id="paragraph_92">better than the one we were left with</div><div class="zn-body__paragraph" data-paragraph-id="paragraph_23B12E93-0D6E-B70C-3CA7-222225150295" data-act-id="paragraph_93">Every breath from my bronze-pounded chest,</div><div class="zn-body__paragraph" data-paragraph-id="paragraph_82ACB2A0-4220-FE0A-00E8-222225230D39" data-act-id="paragraph_94">we will raise this wounded world into a wondrous one</div><div class="zn-body__paragraph" data-paragraph-id="paragraph_28DE3A67-1D7F-0671-3401-2222252CF110" data-act-id="paragraph_95">We will rise from the gold-limbed hills of the west,</div><div class="zn-body__paragraph" data-paragraph-id="paragraph_6080C9C8-81E0-800A-0D65-2222253653B1" data-act-id="paragraph_96">we will rise from the windswept northeast</div><div class="zn-body__paragraph" data-paragraph-id="paragraph_31C4541C-8C4A-2208-5A51-22222547F53B" data-act-id="paragraph_97">where our forefathers first realized revolution</div><div class="zn-body__paragraph" data-paragraph-id="paragraph_5D2FE2F4-3ABA-9092-35CD-222225517BF4" data-act-id="paragraph_98">We will rise from the lake-rimmed cities of the midwestern states,</div><div class="zn-body__paragraph" data-paragraph-id="paragraph_2EF03A88-FD7C-015A-56F9-222225606F36" data-act-id="paragraph_99">we will rise from the sunbaked south</div><div class="zn-body__paragraph" data-paragraph-id="paragraph_8C4C77A4-302D-912B-368D-22222569F8D0" data-act-id="paragraph_100">We will rebuild, reconcile and recover</div><div class="zn-body__paragraph" data-paragraph-id="paragraph_6AC3A2FE-694F-4E22-1DAB-22222579A5D4" data-act-id="paragraph_101">and every known nook of our nation and</div><div class="zn-body__paragraph" data-paragraph-id="paragraph_0A853016-7C0D-BC59-80E5-222225822DCE" data-act-id="paragraph_102">every corner called our country,</div><div class="zn-body__paragraph" data-paragraph-id="paragraph_1E90B3D0-0D1E-94E1-4D1E-2222259084E0" data-act-id="paragraph_103">our people diverse and beautiful will emerge,</div><div class="zn-body__paragraph" data-paragraph-id="paragraph_4A9DE12E-32E3-46F4-06CA-2222259C0C8F" data-act-id="paragraph_104">battered and beautiful</div><div class="zn-body__paragraph" data-paragraph-id="paragraph_B6A6BC0F-C9FF-96C0-5DAC-222225ABA257" data-act-id="paragraph_105">When day comes we step out of the shade,</div><div class="zn-body__paragraph" data-paragraph-id="paragraph_C132E8C4-91DC-8CCB-72C7-222225B78F49" data-act-id="paragraph_106">aflame and unafraid</div><div class="zn-body__paragraph" data-paragraph-id="paragraph_7DA21AA5-CAF8-AD36-CCF4-222225C7B12F" data-act-id="paragraph_107">The new dawn blooms as we free it</div><div class="zn-body__paragraph" data-paragraph-id="paragraph_59E8B9CE-7229-8F6C-D411-222225D2ECA8" data-act-id="paragraph_108">For there is always light,</div><div class="ad ad--epic ad--mobile" data-ad-text="show"><div data-ad-id="ad_rect_btf_01" data-ad-position="mobile" data-ad-refresh="default"></div></div><ul class="cn cn-list-hierarchical-xs cn--idx-115 cn-zoneAdContainer" data-layout="list-hierarchical-xs"></ul><div class="zn-body__paragraph" data-paragraph-id="paragraph_5E2769BF-DB6E-B233-D2B9-222225E4F548" data-act-id="paragraph_109">if only we're brave enough to see it</div><div class="zn-body__paragraph" data-paragraph-id="paragraph_C45B07D3-2196-7C6B-F172-222225F41F3B" data-act-id="paragraph_110">If only we're brave enough to be it</div></div>


Thanks to 
- https://github.com/estelle/html_elements
