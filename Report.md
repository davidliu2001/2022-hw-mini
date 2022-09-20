Hardware Mini Project
David Liu    

Screenshot of code change: 
![Screenshot 2022-09-20 171425](https://user-images.githubusercontent.com/74436905/191365841-334c7df4-8005-4cef-8820-c79523bcb2b8.png)
    
    The code that was changed was in the going up if statement. Two new variables were introduced prior to this which are fade_timer and timer_is_running. In the if (going up) statement the if (fade > 255) was changed to be if (fade > 255 || timer_is_running == 1). By default it only is true when fade reaches a value over 255. Then in the code when fade = 255 the if (fade_timer < 400) is true and increments the fade_timer and makes the timer_is_running variable = 1. This makes it so even though fade is no longer greater than 255 the if statement is still true in the loop and the fade timer is still incrementing until it is over 400 and then gets set back to - and going_up is equal to false. Incrementing the fade_timer variable is purely used to make the led stay at its peak brightness for a longer amount of time and then fade back down. 

    This ended up being successful and was clearly different compared to the default fade code. This success was only after a series of failures with me realizing that I used the wrong cmake compile command (cmake -B build instead of cmake –build build), sleep_ms did not have the desired effect that I wanted and just turned the led off the entire time, and that I used a charge only usb mini cable instead of a data for the longest time. 



https://user-images.githubusercontent.com/74436905/191365933-a2208413-5a75-46d9-9765-647ffdc05fca.mov



https://user-images.githubusercontent.com/74436905/191365935-7dfad007-5dd8-417a-a958-d018174c59e4.mov

