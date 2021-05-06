# toggle-switch
This little project was initiated to investigate how to create a toggle switch that slides along a track when clicked by the user.
It's funny what unexpected things you learn when takling the simplist of things. In this project we first started by attempting to
to animate the slide from ```justify-content:flex-start;``` to ```justify-content:flex-end;``` as it turned out, you can't animate
such values. A sad moment of realisation! Someone (on stackoverflow) suggested that we should probably use something like ```margin-left``` to
transition the slider. The result of using that approach can be seen in ```index.html``` & ```switch.css```. Now, there was a real
downside to doing it this way, as applying ```margin-left``` completely destroyed the original simple design and thus, had to be
completely re-written. Think "unhappy bunny" time!

So check out the result with ```index.html``` & ```switch.css```

Now! having done that (and after spending the best part of a day grappling the the new css) someone else posted a simple solution
to our problem on stackoverflow. Instead of trying to use ```justify-content: flex-end``` it simply used ```flex: 1 1 0%;``` which
is a ```flex-grow``` property that we had not used before, we're really not too familiar with flex and have only really used it
so that we can position things vertically and horizontally without a headache!

Thanks to https://stackoverflow.com/users/11774872/prakash-m for the simple solution.

So check out the result with ```indexToOriginalCSS.html``` linked to ```switch-original-fixed.css``` The original design remains
unaffected and in some ways, much easier to work with. It was kept simple just to post the code on stackoverflow, but I think you
will find that you can do a lot more with that design than you can with the latter.

Oh! One thing! The toggle switch is completely responsive horizontally, which was the cause of the problem, as we wouldn't have a
specific value to move the slider to. So how do you move something to an unknow end position? Here are two ways, we hope they are
of some use.
