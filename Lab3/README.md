## Lab #3: G8RTOS Scheduler and Synchronizers
- Part A: Setting up driver packages and OS structure
- Part B: Implementing thread structures, exception handlers & schedulers 
- Part C: Implementing semaphores & peripheral controls
- Part D: Adding threads for sensor feedback
- Part E: Putting it all together!
- Bonus points: Convert thread0 to use the magnetometer and map to the blue LED for its bearing


## Pointers
* [G8RTOS Hands-on](https://youtu.be/Iru-JiXH2c8)  
* [Walkthrough video](https://youtu.be/uBvrZMxoyzE)
* [Sample interfacing demo](https://youtu.be/huqvGCKN_bU)  


### BMM150 Datasheet For Lab3 Extra Credit
- [Bosch-boschsensortec](https://www.bosch-sensortec.com/media/boschsensortec/downloads/datasheets/bst-bmm150-ds001.pdf)

### Will we use PSP? 
- To utilize the PSP (process stack pointer) on ARM processors, additional configuration needs to be done that we don't do for this class. For all operations in assembly, using the mnemonics SP, PUSH, and POP is sufficient. 

### Floating point operations cause issues with thread switching
- You can wrap floating point operations in critical sections
- Or you could also do a floating point operation at the start of main.

### Relocating Interrupt Vector to SRAM
- For the purposes of this class, the library functions that register an interrupt will automatically relocate the table for you. It is not necessary to relocate the table yourself.