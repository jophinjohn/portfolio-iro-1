---
layout: post
title: Blochat
thumbnail-path: "img/chat.jpg"
short-description: BloChat is an app that use Firebase to build an application that sends and receives messages in real time.
---
<p>Summary</p>

<p>BlocChat is a single-page chat application I made at Bloc program. It was written in 2 months, using Angular JS as the framework. It was also my first time using Gulp as a build tool and npm for package management. I used Firebase as a real time database service.
<a href="https://github.com/jophinjohn/blochat">View Code</a></p>

<p>AngularJS</p>

<p>After I finished BlocJams, I was given a choice of frameworks to learn for the projects phase at Bloc. The cleanliness of the syntax, particularly of AngularJS, appealed to me. It was also "new", relatively, and Angular2 was on the horizon, so I felt compelled to future-proof my education.</p>

<p>Grunt</p>

<p>Before I started BlocChat, I wanted to evolve my method of deployment. In BlocJams I used <script> tags to inject my code into .html files. While that method worked, I knew there were better solutions out there. I was also interested in using live-reload to save time. With hundreds of plugins to choose from , this would eventually aide in my goal of automating tasks in the future. A lot of companies like Adobe and Microsoft use Grunt as their go to for real time visuals. If someone hasn't already built what you need, authoring and publishing your own Grunt plugin to npm is a breeze. For these reasons Grunt was my choice of deployment.</p>

<p>HTML, CSS and Bootstrap</p>

<p>I began by blocking out BlocChat using only HTML and CSS. Once I had the look and feel down, I converted the HTML into Angular JS components. Bootstrap is a CSS framework used to build pages faster. Bootstrap provides a lot of useful CSS out of the box. This is why I had chosen bootstrap for faster development and fast loading of pages and built in CSS elements like Jumbotron for highlighting HTML in a box.
    I had already split BloChat into two main components,HomeCtrl  and Modulectrl; while creating the prototype, so they naturally took on the role of controller-views. Initially I had difficulty using modals through the module ctrl but as time went by I had figured to use modals without using a controller in the template.html with ease. Eventually I plan on revisiting the Blochat app and add in a UserCtrl file so as to give the ability to sign in  and out rather than add users on the fly. 
On the model side, I started with two stores, Rooms and Messages, one kept track of rooms, the other kept track of messages. As the application grew, I also added a cookie to remember information about the user. 
I would say that I understood how closures worked by the time I started BlocChat, but it was using them in my application that made me see their power. Passing functions to components via props was a liberating experience, because I could give responsibilities to UI components without ever making them aware of a world outside their own module. The controller-views were smart, the leaf components were dumb, but there were no sacrifices that had to be made in terms of complexity or functionality on either the view or model side.
The workflow can be dizzying, and it was made worse when multiple components might be listening to a single store. In the case of BloChat, I'm glad I was consistent in naming my files; I feel it went a long way to help me keep track of my modules' relationships.</p>

<p>Firebase</p>

<p>Unlike many chat applications, BlocChat rooms are persistent; all messages that were ever typed in a room are stored in the cloud. Bloc suggested using Firebase to persist data, and in this case I felt no reason to stray from the script. I have only a little experience with SQL, so using a full-featured cloud service was more time-efficient.
The first time I tried to communicate with Firebase, I ran into a problem where the Dispatcher would attempt to resolve two actions simultaneously, which is apparently forbidden. It was here that I really learned the difference between "synchronous" and "asynchronous". When I clicked a button, I naively sent a write action to the dispatcher (to add a room locally) and a write request to the server (to add a room on the server). Since I was listening to the server for changes to the rooms, and using actions to send these changes to the stores, the two resultant actions collided in the dispatcher. The lag on his end acted like an unintended setTimeout().
Once I routed all Firebase-related actions through ChatAPI, my server-communication workhorse, the problem was solved.</p>

<p>Modal</p>

<p>Being new to web development, I had no idea what modals were called but always thought they were really neat. I implemented my own for BloChat for room creation and changing the username. While it worked, the experience wasn't as smooth as I'd have liked, and it was extremely limited. Nesting animations was a big headache and buggy to boot. Eventually I settled for using modals as a separate div in the template.html and it was very easy to work with rather than use it through a controller.</p>

<p>Conclusion</p>

<p>Compared to BlocJams, BloChat felt more "real". I wrote the app from scratch, and integrated Firebase independently. At the same time I was using a proper framework with Angular JS, and professional tools like gulp and npm. The result was a clean, well organized code base for a working chat client. I am proud of it, even though I didn't have time to implement more features I had in mind. Some day I might revisit BlocChat to extend it further.</p>


