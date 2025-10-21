---
title: You Should Be Refactoring
---

A software engineer's work should mainly consist of refactoring. Well, maybe not
in an ideal world where you and your coworkers wrote good code from the start,
and that's a world I want to live in, but we don't live in that world, and most
of the code we deal with was not designed to support the features we want to add
or even the features you've already added, so we (you and I) should be
refactoring.

In a good codebase, bugs are straight-forward: typos (hopefully rarely) or
runtime conditions you didn't anticipate. They might not be easy to fix, but
they should be easy to spot once you know they're there. Is that too much to ask
for? Apparently so. If you stare at your code for half an hour and can't see the
bug, then that's a readability problem. At some point, you just have to clean
your room because it's too hard to find stuff---and then maybe learn to keep it
clean in the first place. If you're working in a messy room, organize it before
adding to it. If you "don't have the luxury" of organizing your room because
you've already spent too much time putting out the fires started by shorting
wires in the "utils" folder, and you hurt your foot on the mousetrap a coworker
put near the charcuterie board that the same coworker added a couple years back
to woo a customer and can't remove because it has since become load-bearing,
then you should take a step back and really think about the situation because
you're doing engineering completely wrong.

Stop saying that engineering work is supposed to "bring value". It's true, but
it doesn't bring value the way you think it does. If you think, "adding this
feature will make our chances at this $1,000,000 contract go from 50% to 70%, so
the feature's expected value is $200,000" then I'm talking to you specifically.
And you too over there, saying how "working on tech debt will reduce bugs by 10%
and improve velocity by 20%." We agree that cleaning up is important, but _you_
came up with fake numbers because tech management can't make decisions without a
dashboard. And _I_ made a blog post about it instead.

Look, I get it, you have a goal, you're trying to make money for your company's
make-more-money KR. But adding random crap that breaks within a year is not how
you go about it, and it's not what your customers want. They want the random
crap to work. No amount of testing now can prove that the crap will work later.
You need to carefully examine your crap---maybe get one of those Dutch
toilets---and then reshape it so that you can tell by looking at it that it will
flush as intended.

Toilets aside, you'll waste a lot more time fixing bad code than you will trying
to write good code. But worse, the amount of time it will take you to fix bad
code scales more than linearly: twice as much bad code takes more than twice the
time to fix. I'd estimate it scales quadratically or worse because of the
frequent hidden coupling in poorly written code: any bad piece of code could
interact with any other bad piece of code, and you don't know because it's
definitely poorly documented, so you have to think about all these interactions
to avoid breaking stuff. It could be even worse than quadratic because sometimes
three or more components have some hidden interaction. The second easiest time
to refactor is now.
