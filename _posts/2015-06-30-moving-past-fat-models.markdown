---
layout: post
title:  "Moving Past Fat Models"
date:   2015-07-01 22:53:45
categories: ruby rails refactor
---
As the Rails community has evolved there has developed ideas and standards about how to write maintainable code. A buzzword in the rails community has become "skinny controllers fat models". What this means is that we avoid putting logic in our controllers, keeping them very small. Instead we place our logic within the models. For the longest time this was standard advice in the Rails community. Many new programmers do not do this and end up having controllers filled with logic that is in no way related to the controllers primary function. However as projects grow this mantra begins to fall short of it's intended goal. The complexity of the code kept in the model beings to grow and soon enough can become confusing and unwieldy. Once a project reaches this point we must look beyond the model for how to structure our code.

Other than general clutter there is a fundamental problem with large models. In many cases this code violates the single responsibility principle. The model's primary purpose is to deal with persistence. Unfortunately code placed in models often has nothing to do with persistence. To fix this we must instead rely on smaller, more cohesive groupings of code.

So what's the solution? To use modules and concerns? This seems like a good idea but this strategy actually causes it's own concerns (pun not intended). By including logic as concerns the methods within are still largely dependent on whatever classes are including them. Instead of being able to test and use the pieces in isolation they could only be used within their respective model. So while it may look much nicer to have code separated between multiple files it does not truly solve our problem. The real solution to this problem is to favor composition over inheritance. In part two of my blog series on refactoring we will dig into what this means.
