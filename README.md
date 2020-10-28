# Mach3Mill-AutodeskHSMProbing-PostProcessor
I have created a post processor for the Mach3Mill that allows you to use the probing operations in Inventor HSM and Fusion.

I used Visual studio code and the "Autodesk Fusion 360 Post Processor Utility" extension to test the syntax of the post processor and the Mach3Mill software in conjuction with a China6040 CNC to check if it works functionally.

There are existing software that has been able to convert the probing operations in Inventor HSM and Fusion to Mach3Mill operations using Mach3Mill Macros. This can be found here -> http://www.mlmsolutions.biz/fusion_post_mach3_probing.php. Martin Marriott has done alot of good work here so I recommend you give it a try first.

Unfortunately I was never able to get this to work and thus decided to create my own Macro free version which uses the inbuilt probing function in Mach3Mill - G31. I believe this method will have its limits of which I will document.

I used the following sites and documents as refrence:
- https://cam.autodesk.com/posts/reference/index.html
- https://cam.autodesk.com/posts/posts/guides/Post%20Processor%20Training%20Guide.pdf


| Probe Type | How It Works | Limits | Future Changes |
| - | ---------------------- | - | - |
| probing-z | - Reset z offset <br> - Stop program <br> - Set feed rate <br> - Probe in -ve z direction <br> - Set new offset | At the moment it will only probe surfaces that should be at zero. <br> Will only probe in the -ve z direction | Will implement it so that it can probe and z plane surface |

## Current Implementations
- probing-z

## Future Implementations
- probing-x
- probing-y
- probing-x-channel
- probing-x-channel-not-symmetric
- probing-x-channel-with-island
- probing-x-wall
- probing-x-wall-not-symmetric
- probing-y-channel
- probing-y-channel-not-symmetric
- probing-y-channel-with-island
- probing-y-wall
- probing-y-wall-not-symmetric
- probing-xy-inner-corner
- probing-xy-outer-corner
- probing-xy-circular-hole
- probing-xy-circular-hole-with-island
- probing-xy-circular-boss
- probing-xy-circular-hole-with-z
- probing-xy-circular-hole-island-with-z
- probing-xy-circular-boss-with-z
- probing-xy-rectangular-hole
- probing-xy-rectangular-hole-with-island
- probing-xy-rectangular-boss
- probing-xy-rectangular-hole-with-z
- probing-xy-rectangular-hole-island-with-z
- probing-xy-rectangular-boss-with-z
- probing-xyz-corner
- probing-x-plane-angle
- probing-y-plane-angle

