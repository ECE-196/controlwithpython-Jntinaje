### How does the DevBoard handle received serial messages? How does this differ from the naïve approach?
  
To start , the board gets an interrupt when new data available, it is then held in temp storage and then after it is stored, it is then processed. It differs from a naive approach because a naive approach may process once data is received a way less secure method. 


### What does `detached_callback` do? What would happen if it wasn't used?

Basically it is like running the function f inside a new thread. It sounds similar to parallelism in ECE 30 where you’re trying to optimize performance by having two functions run at the same time. IN summary like f is running at the same time as main just in a different thread. If we didn’t use this thread we would have to wait for f to finish before continuing running the rest of our main code.  

### What does `LockedSerial` do? Why is it _necessary_?

When a program tries to have multiple parts using the serial port at the same time, it can get a little hectic so that’s where locked serial comes into play. So The locked serial makes sure only one part of the program is read or written to the serial port at a time. It is necessary because without it , a mix match of storing reading or writing data can happen.﻿
