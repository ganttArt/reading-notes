# CF 401 PreWork

## Readings

### [Solving Problems](https://simpleprogrammer.com/solving-problems-breaking-it-down/)

Too often people just jump into coding challenges. Here is a recommended step by step approach to solving these problems:

1. Read the problem completely twice.
1. Solve the problem manually with 3 sets of sample data.
1. Optimize the manual steps.
1. Write the manual steps as comments or pseudo-code.
1. Replace the comments or pseudo-code with real code.
1. Optimize the real code.

### [Act like you make $1000/hr](https://medium.com/swlh/pretend-your-time-is-worth-1-000-hour-and-youll-become-100x-more-productive-f04628bb3e6d)

Takeaways:

- Don't do thankless work for ungrateful takers that don't deserve your time and energy
- Don't be busy for the sake of being busy, duh.
- Extremely successful people don’t tolerate busywork or distraction. They have crystal clear vision on their goals, and do what they need to do to get there, every single day.
- If you let people know your time is free and low-valued, people will treat it as such. But if you teach people that your time is expensive, important, and valuable, then people will respond in kind.
- “The difference between successful people and really successful people is that really successful people say no to almost everything.” -Warren Buffet

### [How to think like a programmer](https://medium.freecodecamp.org/how-to-think-like-a-programmer-lessons-in-problem-solving-d1d8bf1de7d2)

What to do when you encounter a new problem:

- Understand the problem: Know exactly what is being asked. Most hard problems are hard because you don’t understand them.
- Plan your solution with exact steps
- Break the problem into sub-problems
- The best programmers are more curious about bugs than irritated by them
  - When you're stuck: debug, reasses and research

Finally: If you practice and you will get better at solving problems.

### [The 5 Whys](https://www.mindtools.com/pages/article/newTMC_5W.htm)

- The 5 Whys strategy is a simple, effective tool for uncovering the root of a problem. You can use it in troubleshooting, problem-solving, and quality-improvement initiatives.
- The method put simply, is asking why 5 times.
- Here is a process that follows the approach of the 5 whys
    1. Assemble a team
    1. Define the Problem
    1. Ask why this problem is happening. 5 times. Extend your search as multiple possibilities come up.
    1. Know when to stop and when to keep going
    1. Address the root cause(s)
    1. Monitor your measures to make sure they are truly solving your problem.

---

## Videos

### [What the heck is the event loop anyway](https://www.youtube.com/watch?v=8aGhZQkoFbQ)

Chrome V8 - Behind The Scenes

![Chrome V8 - Behind The Scenes](images/ChromeV8.png)

- JS is single threaded, has a single callstack, and thus does one thing at a time
- `Stack Trace` - the state of the call stack that shows up when an error pops up
  - Top one listed is where the error happened, and then below it you can trace what happened to get to this error (what the call stack looks like when your error occured)
- `Range Error: Maximum call stack size exceeded`
  - Most likely due to a function calling itself and those returns never getting resolved
- Blocking: Things on the stack that are taking a long time and thus are slowing other things down
- When js needs to use a web api like setTimeout, once the browser's web api has completed its task it is pushed to the task queue. If the call stack is empty, the event loop takes the first thing in the queue and moves it into the call stack.
- Can wrap a function in setTimeout to 0 time, just so it runs after the call stack has been cleared.
- Two definitions of callbacks. One is a function that another function uses. The other is an async function that utilizes the callback queue.
- Filling up the call stack blocks the browser render. Filling up the callback queue quickly/temporarily blocks the render, but then allows the render occur on and off while the callback queue is gone through
- Don't block the event loop, basically means to not fill up your call stack so things aren't being rendered anymore.
- This has big implications for things like image manipulation/processing. If you are doing a big change to your image, your call stack will be blocking the event loop until the processing is done.
- Make sure you don't flood the callback queue with events. Example shown, having an animation on scroll. If you are scrolling all the time through the site, the callback queue is getting flooded with events it needs to handle. So do some checking with something like this.

### [The Super Mario Effect](https://www.youtube.com/watch?v=9vJRopau0g0)

- You could be more successful if you don't concern yourself with failure.
- More people succeeded at a problem if they were not penalized for failing.
- The Super Mario Effect: Focusin gon the Princess and not the pits, to stick with a task and learn more
- The focus was beating the game, not focusing on everytime you fell in a pit, and you eventually got better
- You need to want to solve the problem. You shouldn't feel like you have to endure everything to just succeed. You shouldn't force yourself to be an optimist. You should work on problems that you want to solve!
- Successes feel better when you've strugged and failed your way there.

[<== Back](../README.md)