---
title: "Progress update by Mark"
date: 2019-04-10T11:46:37+01:00
author: "Mark"
---

Before I get into this week's post, I just want to say thank you to Maru at Unity, who sent Ben a package of Unity swag that
arrived on his eighth birthday. That was a lovely gesture and it made Ben very happy indeed.

We've added or improved a couple of features to Club Penguin Sea since the last post. The one I want to tell you about today
is the clothing system. My next post in a couple of days will be about every parent's favourite gaming trend: in-game currency.

## Clothing

Cosmetic items are an important part of modern games, for reasons that, to be honest, are kind of lost on me. If you happen to race
me on Forza Horizon 4 online, after the race I'll be the one in whatever the default clothes were, with no "emote". I'm 46. I'm boring.

But my kids are nuts for this stuff, and so we had to add it to CPS. We got the first thing (a rubber ring with a duck head) added easily enough.
I added an empty GameObject to the Penguin prefab, and added a SpriteRenderer component to that. Then I set the Sprite to the rubber ring, and
added some code to turn it on and off in the Clothing Shop when the penguin is in contact with the display item and you press the Interact button.

The next "clothing" item Ben drew was... a car. And he had a bunch more to add as well. I didn't want to be adding GameObjects for every
possible item of clothing, so I put on my Professional Developer Head and came up with a proper, reusable solution that has worked very well.

I unset the Sprite property from the clothing object's SpriteRenderer, and changed the code to set that property from the shop's display item.
I loaded up Affinity Photo, which we use for working with Ben's hand-drawn graphics, and changed the rubber ring sprite to be the same size
as the penguin sprite (320x480) with a transparent background. Then we made sure that the ring itself lined up correctly with the penguin, and
re-exported the sprite. When we switched back to Unity and set the Sprite property, the ring lined up perfectly! Now for the next test.

I went through the same process with the car, making sure the sprite was the right size and lined up with the penguin. Just for good measure,
I added a very low-opacity blue tint to the windscreen. Then we exported that sprite, dragged it onto one of the pedestals in the clothing
shop, and ran the game. And it worked!

![Penguin and Car sprites in Affinity](/images/clothing/carinaffinity.jpg)
<small>Penguin and Car sprites in Affinity</small>

So now, any time Ben draws new clothing, that's all we have to do. Create a transparent 320x480 PNG image with whatever it is in the right
place (we use a locked layer with the Penguin image to line things up), drag it into the clothing store scene, and *It Just Works*.
There's no extra code to write, no fiddling with empty GameObjects or anything. And the other big advantage to this is that we have a nice,
big visual editor for positioning the sprites, so Ben can easily tell me where things are supposed to go on the penguin.

Here's our latest gameplay video:

{{< youtube N6yn4HB2WE4 >}}

