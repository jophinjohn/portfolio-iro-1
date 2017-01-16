<p>--
layout: post
title: BlocJams
thumbnail-path: "img/logo.jpg"
short-description: Bloc Jams, a digital music player like Spotify
 --</p>

<p>Summary</p>

<p>BlocJams was a crash course on the basics of frontend development, from language and tools to workflow and design. I was exposed to Git, text editors, HTML, CSS, JavaScript, jQuery all in the span of 2 months.
<a href="https://github.com/jophinjohn/intro-to-angularjs">View Code</a></p>

<p>The Tools</p>

<p>The project began with an introduction to text editors and Git. The syllabus creators at Bloc recommend Brackets, which is what I used. At Bloc I resolved to become learn to use CLIs. The going was rough at first; I would often mess up commit messages, leading to liberal uses of --amend. The commits themselves were messy, with many small vaguely related changes, and sometimes I wrote the wrong message entirely. The rules I followed were:</p>

<ol>
<li><p>Don't commit to the master/main branch</p></li>
<li><p>All branches should branch off of master</p></li>
<li><p>Merge branches to master via Pull Requests on GitHub, then pull to local master</p></li>
<li><p>Sync branches with 'git rebase'</p></li>
<li><p>Try to work on one branch at a time</p></li>
</ol>

<p>Moving from GUIs to CLIs was rocky process, and I still feel more comfortable in a GUI environment, but I've since lost my anxiety over command lines. Using Git through a terminal has also taught me more about how Git actually works than Tortoise ever did.</p>

<p>HTML and CSS</p>

<p>I toured modern HTML and CSS by creating a static mockup of the target product with a landing page, a collection page, and an album page. I had some prior experience with both languages so this segment was more of a refresher than a learning experience. Semantic tags like <section> and <nav> were new to me, and seemed like a reasonable feature at first, until I thought harder about what a <section> really was. I found resources like HTML5 Doctor to guide my understanding, but eventually came to the conclusion that my time was better spent on fleshing out the project.</p>

<p>I learned more in creating BlocJam's CSS. Transform was a big surprise; they didn't exist in 2011, and that was when I picked up CSS. Being able to treat my block elements like objects in a game engine was pretty amazing, and transitions even more so. Suddenly, many snappy animations websites use were demystified. I was under the impression web animation used to be done with scripts, so it was a pleasant surprise to discover I could move between the most common CSS properties with something as clear and simple as a transition.</p>

<p>Another moment of revelation was the discovery of media queries. I had absorbed terms like "responsive design" via osmosis, but had no idea what they referred to except that sometimes a website would adapt itself to my device's display size. I always thought the adaptation was achieved with multiple style sheets, and perhaps they once were, but now the problem has a more robust solution in media queries.</p>

<p>From C++ to JavaScript</p>

<p>With the mockup done, I went through the process of adding functionality to the project like triggering CSS transitions, animating the seekbar, storing data inside nested objects, and DOM manipulation. Meanwhile, I was picking up JavaScript at a rapid pace.</p>

<p>I didn't understand the need for ===, until I learned of JavaScript's automatic conversion between its primitives. Strict equality made a lot more sense once I viewed it in the context of var's dynamic nature. Prototype inheritance was another case of culture shock where an unfamiliar, flexible system took the place of one that was rigorously structured.
I had encountered closures through C++11 (called lambdas) before. They didn't click immediately, and I never understood the benefits of closures until I delved into JavaScript. Being able to pass around functions as easily as objects made programming the UI much simpler than I was used to. </p>

<p>To actually give BlocJams full music player functionality, I refactored the entire project with jQuery, which cut down the verbosity, and I integrated the Buzz library so the site could actually play music. Integrating Buzz wasn't a big challenge, and gave me a taste of the vast array of plugins and third-party libraries available to frontend developers.</p>

<p>Conclusion</p>

<p>BlocJams was a very instructive project. I covered more ground in 2 months than I have in an entire semester of some of my college courses, especially Introduction to Web Development. I'm glad I entered Bloc with a few years of programming under my belt; I might've been overwhelmed by the pace as a total novice. BlocJams used <script> tags to insert all of its code into index.html. Functions were defined in the global scope. Even with the power of lambdas and jQuery, I would definitely describe some of the .js files as "spaghetti code". The next project and involvement of Angular helped me overcome this limitation. </p>

<p>Addendum with reference to Angular:</p>

<p>General differences.</p>

<p>The above points are aimed at the OP's specific concerns. I'll also give an overview of the other important differences. I suggest doing additional reading about each topic as well.</p>

<p>Angular and jQuery can't reasonably be compared.</p>

<p>Angular is a framework, jQuery is a library. Frameworks have their place and libraries have their place. However, there is no question that a good framework has more power in writing an application than a library. That's exactly the point of a framework. I  could write your code in plain JS, or can add in a library of common functions, or can add a framework to drastically reduce the code you need to accomplish most things. Therefore, a more appropriate question is:</p>

<p>Why use a framework?</p>

<p>Good frameworks can help architect your code so that it is modular (therefore reusable), DRY, readable, performant and secure. jQuery is not a framework, so it doesn't help in these regards. We've all seen the typical walls of jQuery spaghetti code. This isn't jQuery's fault - it's the fault of developers that don't know how to architect code. However, if the devs did know how to architect code, they would end up writing some kind of minimal "framework" to provide the foundation (achitecture, etc) I discussed a moment ago, or they would add something in. For example, you might add RequireJS to act as part of your framework for writing good code.</p>

<p>Here are some things that modern frameworks are providing:</p>

<p>• Templating</p>

<p>• Data-binding</p>

<p>• routing (single page app)</p>

<p>• clean, modular, reusable architecture</p>

<p>• security</p>

<p>• additional functions/features for convenience.</p>

<p>The next project refactored the code in AngularJS to finish up the same BlocJams in very little time. Albeit a bit more complex at times , development time was drastically cut short.</p>


