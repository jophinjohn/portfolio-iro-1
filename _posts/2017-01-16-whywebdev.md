---
layout: post

title: My goals as a web dev
---

<p>Don’t just solve problems, figure out what’s really going on</p>

<p>Too many people who write CSS and JavaScript tinker until they find something that works, and then they just move on. 
I’ll frequently ask: “Why did you add float: left here?” or “is this overflow: hidden really necessary?”, and respond: “I don’t know, but if I remove it, it doesn’t work”.
The same is true of JavaScript. I’ll see a setTimeout being used to prevent a race-condition, or someone stopping event propagation with no regard for how it will affect other event handlers on the page.</p>

<p>I get that there are times when you need something that works, and you need it now. But if you never take the time to understand the root of your problem, you’ll find yourself in the same situation over and over again.
Taking the time to figure out why your hack works may seem costly now, but I promise it’ll save you time in the future. Having a fuller understanding of the systems you’re working within will mean less guess-and-check work going forward.</p>

<p>Learn to anticipate future changes to the browser landscape</p>

<p>One of the main differences between front and back-end code is back-end code generally runs in an environment that’s under your control. The front end, by contrast, is completely outside of your control. The platform or device your users have could completely change at any moment, and your code needs to be able to handle that gracefully.
I understand that in the real world feature detection doesn’t work 100% of the time, and sometimes you have to depend on buggy behavior or whitelist browsers whose feature detects erroneously return false positives (or negatives), but any time you do this it’s absolutely critical that you anticipate the almost-certain future where these bugs no longer exist.</p>

<p>Read the specs</p>

<p>There will always be browser bugs, but when two browsers render the same code differently, people will often assume, without checking for themselves, that the so-called “good” browser is right and the “bad” browser is wrong. But this isn’t always the case, and when you’re wrong about this assumption, whatever workaround you choose will almost certainly break in the future.
A timely example of this is the default minimum size of flex items. According to the spec, the initial min-width and min-height value for flex items is auto (rather than 0), which means by default they shouldn’t shrink to smaller than the minimum size of their content. 
When two or more browsers render the same code differently, you should take the time to figure out which one of them is correct and write your code with that in mind. Your workarounds will be far more future-proof as a result.
In addition, so-called “great” front-end engineers are often the people on the forefront of change, adopting new technologies before they’re mainstream and even contributing to the development of those technologies. If you cultivate your ability to look at a spec and imagine how a technology will work before you can play with it in a browser, you’ll be part of a select group who is able to talk about and influence the development of that spec.</p>

<p>Read other people’s code</p>

<p>Reading other people’s code, for fun, is probably not your idea of a fun Saturday night, but it’s without a doubt one of the best ways to become a better developer.
Solving problems on your own is a great way to learn, but if that’s all you ever do, you’ll plateau pretty quickly. Reading other people’s code opens your mind to new ways of doing things. And the ability to read and understand code that you didn’t write is essential to working on a team or contributing to open source projects.
A great way to achieve this is via Codewars. Once you solve a kata, reading up on other solutions will give a wide perspective of how one problem can be solved many different ways and which solution is the best for particular environment.</p>


