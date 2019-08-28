# KLIC Photo VR 6DOF 

## What is This?

This is a sample VR application for Oculus Quest that builds a virtual art gallery and will even allow someone to buy a custom photo product using our KLIC Photo (Lifepics) API.  KLIC Photo (formerly Lifepics) offers a complete omnichannel ecommerce platform for your photo needs and is used by many photo stores, grocery chains and anyone interested in selling photo products or services.  

This was meant as a starting point and example for our partners on using new channel types to expand user engangement and increase conversion.

Due to licensing issues, I cannot post the source code in a public repo but I have included the APK so it can be loaded.  If you are interested in the source code and are a Lifepics/KLIC Photo partner, just contact us.

If you are interested in building apps like this one against our API, you will want to contact us.  Just send an email to sales@taylordigital.io telling us that you are interested in creating an app or hosting a photo site on our platform.  We offer a complete omnichannel photo solution across Web, Kiosk, and headless options for creative solutions like this one.

You can see a complete video of the app here:

https://www.youtube.com/watch?v=2-utLyy_3PI

## Summary of the VR App

![Unity Editor](http://mobilefission.io/wp-content/uploads/2019/07/UnityEditorScreen.png "Unity Editor")

This app begins by generating a Virtual Reality art gallery based on photos dynamically retrieved from your KLIC Photo Albums via the KLIC Photo (Lifepics) API.   You can actually walk through the gallery using positional tracking and there is some background ambient noise from the National Art Gallery in London so it really feels like you are in a gallery/museum.  The gallery is randomly generated each time you come in to keep it fresh.

![Preview](http://mobilefission.io/wp-content/uploads/2019/08/ezgif-2-8a3189073f7d.gif "Mug Preview")

It also has a dynamic product generator that will create a personalized photo product (coffee mug) you can hold, examine, play with and purchase right within VR based on the photos from your photo library!  Doing this requires real-time manipulation of the base texture for the mug to inject a photo correctly and get it to match what will be produced.   I am not very good at creating 3D models but I found a coffee mug asset that has a photo area with an aspect ratio very close to our Lifepics 11 oz mug.  I was able to tweak this so it matched and it absolutely matches production (I verified this in MediaClip). This is very doable as long as the model created follows some guidelines in how the UV map is created (more on that later).

![Purchase](http://mobilefission.io/wp-content/uploads/2019/07/shopgif.gif "Purchase Preview")

Buying the product is as simple as placing it on the shopping cart pad.  It detects a generated product and allows you to check out with your default shipping address in Lifepics. Similar to the Alexa Skill prototype I created a few years ago, if you want to ship to a different address instead you can simply add the configured item to your cart and you can complete checkout on your computer or phone.  This is thanks to the fact that KLIC Photo is an omni-channel ecommerce system.

I also started creating the beginning of a game that demonstrates the capabilities of Unity (and other 3D engines) to manipulate textures.  Essentially, I randomly pick a photo from your album and make four cubes out of the photo which you have to put together as fast as you can to form the original photo.  This needs some additional development before it is complete but the idea was to try doing some additional texture manipulation in creating other objects including crop, scale and slice.

This looks SO much better in the actual headset versus what I can show you in a video or screenshot, but if you have played with a newer 6DOF VR device before you will get the idea. The gallery canvases actually look really great.  It is neat seeing your photos enlarged in a “real” space and being able to pick up, play with, closely examine and order an actual product with full positional tracking. I spent a lot of time trying to make the most of the hardware so the canvas art and product look very clear up close.  Definitely good enough to decide to buy the product!

## Technical Requirements

This was built using Unity 2019.2.0f1 and the latest Oculus Integration SDK.  It is current targeted to Android (Oculus Quest) but should be easy to target to Windows and the Rift if you desire.

## Sideloading Instructions

If you have an Oculus Quest and want to try it out for yourself, you will need to manually install (or sideload) the application onto your headset.  Instructions for this are available here:

https://uploadvr.com/how-to-sideload-apps-oculus-go/

## Using your Own Photos

To see your own photos in the photo gallery, just create an account on our test site at:

https://photo.cuat.lifepics.com

Once you create an account, create an album by going to the account area and just upload a bunch of photos into it.  The VR App will use your most recent photo album.



