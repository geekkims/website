Skip to content
Search or jump to…
Pull requests
Issues
Marketplace
Explore
 
@geekkims 
nschloe
/
matheon-html5-template
Public
Code
Issues
Pull requests
Actions
Projects
Wiki
Security
Insights
matheon-html5-template/README.html
@nschloe
nschloe initial files
Latest commit 79aa0c6 on Nov 6, 2012
 History
 1 contributor
105 lines (103 sloc)  4.48 KB
 
<h1><img src="images/io2012_logo.png"> HTML5 Slide Template</h1>

<h2>Configuring the slides</h2>
<p>Much of the deck is customized by changing the settings in <a href="slide_config.js"><code>slide_config.js</code></a>.
Some of the customizations include the title, Analytics tracking ID, speaker
information (name, social urls, blog), web fonts to load, themes, and other
general behavior.</p>
<h3>Customizing the <code>#io12</code> hash</h3>
<p>The bottom of the slides include <code>#io12</code> by default. If you'd like to change
this, please update the variable <code>$social-tags: '#io12';</code> in
<a href="theme/scss/default.scss"><code>/theme/scss/default.scss</code></a>.</p>
<p>See the next section on "Editing CSS" before you go editing things.</p>
<h2>Editing CSS</h2>
<p><a href="http://compass-style.org/install/">Compass</a> is a CSS preprocessor used to compile
SCSS/SASS into CSS. We chose SCSS for the new slide deck for maintainability,
easier browser compatibility, and because...it's the future!</p>
<p>That said, if not comfortable working with SCSS or don't want to learn something
new, not a problem. The generated .css files can already be found in
(see <a href="theme/css"><code>/theme/css</code></a>). You can just edit those and bypass SCSS altogether.
However, our recommendation is to use Compass. It's super easy to install and use.</p>
<h3>Installing Compass and making changes</h3>
<p>First, install compass:</p>
<pre><code>sudo gem update --system
sudo gem install compass
</code></pre>
<p>Next, you'll want to watch for changes to the exiting .scss files in <a href="theme/scss"><code>/theme/scss</code></a>
and any new one you add:</p>
<pre><code>$ cd io-2012-slides
$ compass watch
</code></pre>
<p>This command automatically recompiles the .scss file when you make a change.
Its corresponding .css file is output to <a href="theme/css"><code>/theme/css</code></a>. Slick.</p>
<p>By default, <a href="config.rb"><code>config.rb</code></a> in the main project folder outputs minified
.css. It's a best practice after all! However, if you want unminified files,
run watch with the style output flag:</p>
<pre><code>compass watch -s expanded
</code></pre>
<p><em>Note:</em> You should not need to edit <a href="theme/scss/_base.scss"><code>_base.scss</code></a>.</p>
<h2>Running the slides</h2>
<p>The slides can be run locally from <code>file://</code> making development easy :)</p>
<h3>Running from a web server</h3>
<p>If at some point you should need a web server, use <a href="serve.sh"><code>serve.sh</code></a>. It will
launch a simple one and point your default browser to <a href="http://localhost:8000/template.html"><code>http://localhost:8000/template.html</code></a>:</p>
<pre><code>$ cd io-2012-slides
$ ./serve.sh
</code></pre>
<p>You can also specify a custom port:</p>
<pre><code>$ ./serve.sh 8080
</code></pre>
<h3>Presenter mode</h3>
<p>The slides contain a presenter mode feature (beta) to view + control the slides
from a popup window.</p>
<p>To enable presenter mode, add <code>presentme=true</code> to the URL: <a href="http://localhost:8000/template.html?presentme=true">http://localhost:8000/template.html?presentme=true</a></p>
<p>To disable presenter mode, hit <a href="http://localhost:8000/template.html?presentme=false">http://localhost:8000/template.html?presentme=false</a></p>
<p>Presenter mode is sticky, so refreshing the page will persist your settings.</p>
<hr />
<p>That's all she wrote!</p>
© 2022 GitHub, Inc.
Terms
Privacy
Security
Status
Docs
Contact GitHub
Pricing
API
Training
Blog
About
