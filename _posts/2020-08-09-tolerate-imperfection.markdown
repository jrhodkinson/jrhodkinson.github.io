---
layout: post
title:  "Tolerate Imperfection"
date:   2020-08-09 17:00:00 +0100
categories: software
---
Software engineers feel uneasy when things aren't right.

Students or junior engineers are unsettled through unfamiliarity with programming concepts.
Gradually, we are unsettled by abstractions at higher and higher levels.
We're no longer troubled by a lack of understanding, but instead when systems don't conform to patterns we know to be sound, or worse, when systems do conform to patterns we know to be harmful.
Refined unease.

We learn that unease is a reliable indicator that we are heading towards a problem.

Good and great engineers feel this unease.
What differentiates the good from the great? Great engineers listen to their intuition, but use their conscious minds to reason about whether something should be done.
Great engineers cultivate space between unease and action.
Great engineers can tolerate imperfection.

All engineering decisions should be made with an understanding of the business context that surrounds them.
Why is this piece of code being written? This must inform the decisions you make.

Imagine that you are developing a system that operates on some data.
Should you persist some data in a database, an ordered log, or a properties file? Does it need to be persisted at all, or would it be acceptable to recompute it on start? Or even to accept that the data will be lost on restart? In a vacuum, it is impossible to argue fruitfully for one of these solutions over any other.

All of these solutions (and more) are reasonable, depending on the context.
They all have tradeoffs: initial implementation effort, running costs, maintainance, monitoring.
But too often I see engineers choose a too-complicated, too-expensive, option because the stupid-simple solution made them uneasy.

Look, I'm not arguing that you should sleepwalk into tech debt.
I'm saying that when you have many options available to you to solve a problem and the simple option makes you feel uneasy, you should step back and consider _why_.
Often, there's a sound reason why the simple solution doesn't work.
Sometimes there isn't.
When there isn't, you save yourself the trouble of implementing the complex solution, and your teammates the trouble of maintaining it.

Until now, I've discussed only the tradeoffs involved in writing new software.
But the cardinal sin is to reject imperfection in existing code.

Here's the thing: it doesn't matter what decision _might_ have been made before this code was written.
The fact is, it exists.
Often it makes us uneasy.
Sometimes the wrong tradeoff was made.

You have a moral obligation to make the code you work on a better place for future engineers.
However, there comes a point (quickly) where re-engineering existing code is a waste of time.
Do the small things that  make the code more hospitable.
If you want to do anything more, consider carefully.

How many times have you heard a teammate say they're picking up a refactor as part of their ticket only for it to get out of hand and completely halt progress on their primary goal? How many of these refactors are eventually abandoned before completion? How often does this result in two parrallel models for the same thing, making the codebase even more confusing?

There are other advantages to tolerating imperfection.

[You might not really understand why the code is the way it is](https://fs.blog/2020/03/chestertons-fence/).
The original authors might have made the perfect tradeoff, but you can't see that from your position.
Your unease is unfounded and more akin to that of the junior engineer or student.
Always account for the possibility that your intuition is wrong.

Rewriting a junior engineer's code is demoralising.
If a junior has done something that isn't right, don't take it upon yourself to rewrite it.
First, decide if something needs to be done.
Maybe it doesn't.
If it does, see if you can work with the junior to work towards a better solution.
Now this is a positive learning experience.
There is nothing more discouraging than discovering that a senior silently rewrote your code.

You must be able to tolerate imperfection if you are to get anything done at all.
Nothing we ever do will be perfect.
It's a fool's errand to try to make it so.