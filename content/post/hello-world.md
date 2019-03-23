---
title: "Hello World"
date: 2019-03-23T22:23:42Z
author: "Mark"
---

Hello! Welcome to Club Penguin Sea!

This is a project I'm working on with my son, Ben. He's seven years old, and he likes videogames,
YouTube and crisps. He plays a lot of Minecraft, watches other people play Minecraft, and if somebody
acquired the license and made Minecraft-themed crisps, he'd be very, very happy.

Another game that he liked a lot was Club Penguin, and then, when they closed that down, Club Penguin Island.
Then they closed that down, too, which made Ben sad. But then he found the [Club Penguin Rewritten project](https://cprewritten.net/),
so he was happy again. But that also got him thinking...

I'd been doing some game programming with my daughter, Willow, so Ben asked if we could make *our own* Club Penguin,
and of course I said yes. I mean, this is a chance to spend quality time with him, teach him some useful stuff,
*learn* some useful stuff myself, and all while doing what I love doing anyway. How cool is that?

We're making the game in [Unity](https://unity.com/), mainly because I'm an experienced C# programmer, but also because Unity offers
a Personal Edition which is completely free. You only have to start paying for it if you're making more than
$100,000 a year from your games. I think we're still a little way from having to worry about that :)

Our workflow is designed for maximum fun. Ben is bursting with ideas for the game, so I try to pick the ones that
I think we can achieve fairly quickly. He draws all the art in felt-tip pen on plain card. I scan it in,
trim the background in Affinity Photo (so sprites are transparent), and copy it into Unity. Because Unity is a visual game
editor, the time from him drawing it to it being in the game is a couple of minutes. Obviously wiring things up and
writing the code to make things move and interact takes a bit longer, but the feedback loop is very quick and gratifying.

![Hand-drawn background](/images/hello-world/background.jpg)
<small>Original background image</small>

The coding is pretty complicated for a kid who's still learning [Scratch](https://scratch.mit.edu/) and [Hopscotch](https://www.gethopscotch.com/),
but I talk Ben through what I'm doing,
and sometimes get him to work out the `else` part of a branch. For example, we add a number to X to make the penguin move right,
so how might we make him move left? Ben thought about this and said "take away from X?" High five! Then we talked about X being left
and right, and Y being up and down, and wrote the up/down code together. He's learning about functions, variables, objects, all
sorts of things.

So far, we've created:

- The outside, where you can walk around and throw snowballs, and go into three doors to other screens
- The Pet Shop, where you can adopt a Puffle which then follows you around
- The Dojo, where you can play a rock/paper/scissors-style card game against Sensei
- Sled Racer, our most ambitious mini-game so far, where you race down a mountain in a tube
- A clothing store, where you can choose items of clothing for your penguin to wear.

We've probably spent less than 24 hours in total on the project so far, so that's pretty good progress. It's definitely rough and
ready, but it works. Well, it mostly works. Turns out seven-year-olds make amazing testers. We were having an issue with the control 
system where when you hit the back button to exit one of the mini-games, the game exited right out. Turned out to be because loading 
a new scene kept the button press, so I had to write in a delay to prevent the back button from working for a second after a scene loaded. 
I use the same ExitManager component in each scene so I fixed it there, tested it on one scene and called it fixed, to which Ben 
responded "shouldn't we test it on the other doors too?" In this case it did work, but still, good call.

Using Ben's hand-drawn art gives him a real sense of ownership, and makes it so quick and easy to add new stuff. We don't worry about
whether everything's pixel-perfect; we can always come back and change graphics and things later if we need to. Being a non-artistic type
of person myself, the art side of game development has always felt like a big barrier to entry for me when I've thought about making games.
That's not a problem on this project, and maybe that'll encourage me to finally get on and try one of my own ideas, post-bedtime.

![Graphics for the "Card Jitsu" Dojo](/images/hello-world/sprites.jpg)
<small>Graphics for the "Card Jitsu" Dojo</small>

We're now at the stage where every time we complete something we do a proper standalone build and I copy it onto Ben's laptop so he can play it. 
He loves that it's a real thing, just like the other games he has on there, and he can plug in an Xbox controller and play it.
When it's a bit more polished (mainly UI stuff) I'm going to make a WebGL build and put it online so his friends can play, too.

We also make videos and upload them to YouTube every now and then, and Ben's teacher shows them in class. Apparently his friends ask loads of 
questions about the game and how we're making it, or suggest things we could add. Next term I'm going into the school and we're going
to give a talk about it, which I'm really looking forward to.

I posted about this project [on the Unity forums](https://forum.unity.com/threads/making-a-game-with-my-son.646339/#post-4339531), 
and some people suggested starting a blog, so here we are. I'm going to post things
about the process and stuff that I'm learning as we go along, and Ben's going to write his own posts about whatever he wants.
We'll post videos and pictures and stuff too.

Here's our most recent gameplay video:

{{< youtube Iwd7JoLnY1U >}}

More to come soon!