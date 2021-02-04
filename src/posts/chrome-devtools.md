---
title: Let me convince you why you should use Chrome's REAL debugger and not `console.log`
date: '2021-02-03'
tags:
  - blog
---
We've all been introduced to the Chrome DevTools as new devs... heck, even regular users messing around with the browser have discovered the "Inspect Element" tool. As a dev, you will have learned about using `console.log` to print variables and logic to the "console" on the browser. This is all normal in the passage of a fresh web developer, however lot of devs never take full advantage of the Chrome DevTools.

Do you still use `console.log` as your sole debugging tool? There is a high chance that it's wasting you a lot of time when it comes to modern Frontend development for the web.

`console.log` is a viable logging tool, but as a debugger it lacks a lot vision. Let's take some sample projects and compare the two tools.

## console.log

Here's an example of how we could log out json data that our application uses. Take note of how we have to log json out as a string. This means we cannot actually traverse the json; it'll be printed out as a flat string.

![console.log in code](/images/console_log_code.png)

Below is the output we get from logging our product and cart data.

![console.log in devtools](/images/console_log_devtools.png)

The effort it takes to explore this data is a little daunting. It's so easy to get stuck in a bad "debugging loop" with logging data that goes something like this:
```
1. Add logging 
2. Analyze what was logged
3. Realize we need more info
4. Repeat steps 1-3 until bug is found or we have an understanding of the issue
```
This seems like a fine solution for most, but we spend so much time: trying to re-serve the application, figuring out where and when data needs to be logged, understanding how all of the data interacts with itself........

![](/images/sweaty.gif)

## Chrome DevTools

So, how can Chrome DevTools make this process any easier? 

DevTools provides a proper debugger that can be manipulated in real-time. It displays the relevant data when a breakpoint is hit, shows the current call stack, and lets us use all of that in the console with temp globals. If we look back at our "debugging loop", we saved so much time by avoiding spinning up the app and hunting down exactly where to log info from. 

It's all provided in the DevTools: all we have to do is set a breakpoint c:

![](/images/breakpoints_scope.png)

The most useful "feature" that completely sells DevTools for me is that it is time-centric rather than data-centric. With `console.log`, we try to decipher what/when something happened with the information we log. Debugging with DevTools lets us actively walk through the running application, allowing us to see the flow of our data and logic. Example:

![](/images/time_based_debugging.gif)

This feels like a superpower to me. I can actively walk through how my code is executed and watch the data be affected. Doing the same with `console.log` requires a lot of assumptions to be made based on the information logged. I think I've made it pretty clear, Chrome DevTools is a pretty effecient debugger, but that doesn't discredit `console.log`. 

Every tool has its time and place.

## When you NEED to use Chrome DevTools

I'll argue there is one reason we MUST use the Chrome DevTools, and that's to understand network requests. As a web developer, you almost definitely work with REST calls (or any other network related call). Javascript natively does not allow us to hook onto requests. Chrome DevTools to the rescue! Open the Network tab before the request is triggered; it'll record all network calls being made. This has been a lifesaver when it comes to spotting subscription leaks in RxJS, malformed request bodys, request failures, etc.

![](/images/network_request.gif)

## The Truth

Yes, we can absolutely stick to just using `console.log` for all your debugging needs. My first employer runs a web solutions business with over 200 regular clients... he solely relies on `console.log`. I understand he does this due to comfort and feeling in his "zone" logging everything, but if he took an hour to understand the DevTools that come with his browser, his work would be friendlier. 

Chrome DevTools comes with a lot out of the box and that can feel very intimidating. I only described two parts to all of the Chrome DevTools assortment!! As a new dev, this is the main reason we skip using them and never come back. We end up sticking to console logging all our issues in hopes of finding the bug sooner or later.
