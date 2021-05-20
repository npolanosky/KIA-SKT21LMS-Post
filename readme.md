This is the postprocessor for a KIA SKT21LMS. Mine is serial 0134, built in 2003 with a Fanuc 0i-TB control. It is a work in progress and you use it at your own risk. There is no warranty an dwe are not liable for any damage it may cause to your machine. 

There is a known issue right now where it adds extra G28 home moves between operations with the same tool- you may have to remove those manually, but aside from that it works well. Leave most of the post properties alone. I'm still working on removing the ones that aren't relevant since this was originally the Doosan post and designed to support their whole line of machines. 
"Use bar puller" will call my bar puller subprogram and pass some macro variables if checked. Probably not relevant for you but I can share it too if you'd like. 
"Use G28" will toggle between using the G28 home position at the back or G30 at a user-configurable location in the lathe. I have mine set about halfway up the Z travel of the machine to save time on shorter parts. 
Axial and radial milling works great but does not support helical moves in polar interpolation mode. Plunge moves and then circular/linear/arc moves are fine, I've even done 3d surfacing. There's a strange lead-in where the C axis will dance a little, you can ignore that. Rapid moves are not supported in that mode either so it has a high feed of 60ipm set if I remember right. 

Subspindle support is coming. You can post programs for the sub no problem, it will automatically flip the Z coords for you. Program like it's for the main spindle but tell Fusion it's the sub from the setup menu. That works great, but you still have to program any transfer/sync moves on your own for now. I'm working on that, just low on free time lately so I haven't sorted that out yet. If your machine has a tailstock I am not sure how that is handled so use caution. 

If this helped you out, consider tossing me a few bucks for snacks. https://www.paypal.com/paypalme/npolanosky
