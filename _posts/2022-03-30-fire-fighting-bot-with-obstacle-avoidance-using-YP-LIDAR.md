---

layout: post
author: Rishabh
title:  Fire fighting bot with obstacle avoidance using YP-LIDAR
description: A mobile robot with 3-R manipulator with autonomous safety takeover mechanism, which can be teleoperated to extinguish fire. 
categories: [ Robotics, ROS, Python ]
image: https://github.com/rish2911/rish2911.github.io/blob/master/assets/images/pics/intro.png
---
Fires propagate at an exponential speed which makes it utterly necessary to be quick in
action. Since structures like houses and buildings tend to collapse , it is tough to reach
the source of the disaster to extinguish it. The significant factors required to focus on
these situations are speed, robustness, the safety of firefighters, and communication.

The USA is known to have one of the highest fire death rates in the industrialized world
during the past decade. According to the 2019 reports, the local fire departments all
over the country have responded to an estimate of 1,291,500 fires, which have caused
an estimated 3,704 civilian deaths, 16,600 civilian injuries, and $14.8 billion in direct
property damage. To worsen matters, career firefighters have experienced an
average of 20,650 fire-ground injuries each year from 2015 through 2019 and have lost
140 firefighters while on the job in 2020. The adversity does not end, firefighters, who
survive, experience long term consequences from primary fire ground injuries like
strains or sprains (27 percent), smoke inhalation (18 percent), the pain only(12 percent),
thermal burns (7 percent), and cuts or lacerations (5 percent). The above facts are
quite disappointing considering the technological advancements of this era.

In this paper, we propose a compact and portable emergency responder robot that
assists firemen in fighting high-rise fires, especially in highly dangerous environments
where it is not safe for people to enter, called the Fire-fighting Robot. The Fire-fighting
robot is custom-designed to be modular, fire-resistant, and robust. Operated by remote
belly-pack controllers, users are provided a real-time video feed allowing them to
traverse hazardous terrain and push obstacles from their path while withstanding
extreme elements. It utilizes a lidar to get depth knowledge of its surroundings in
real-time. The robot is also programmed to protect itself by keeping a specified distance
from the center of hazard.
This robot will reduce the risk of injury for firefighters and possible victims and decrease
the monetary losses which increase considerably as fire duration increases.


#### Application
![Existing robots doing the job](/assets/images/pics/figure2.png)
Certain tasks are in account when creating robotic firefighting systems. These tasks include evaluating and finding flames, conducting search and rescue operations,
monitoring hazardous variables, and fire management and suppression. Numerous lives can be saved by employing robots in hazardous situations. These include the lives of those affected by the disaster and the people working to save them such as firefighters. This product can be very useful in times of emergency when it is
very dangerous for humans such as the retrieval of hazardous materials. The fire-fighting robot is designed to mitigate life-threatening situations with tools
required for fire suppression, situational awareness, and intelligence gathering. It can identify the location of hazards and operate remotely, giving continuous real-time feedback to the operator. It will sense the fire and spray fire-suppression liquids and chemicals onto that direction until the fire subsides.



#### Robot Type
![SImplified model of our fire fighting bot](/assets/images/pics/figure3.png)
The proposed model is a ground vehicle with a rear drive transmission. The front two wheels are used to steer the robot. A 3-R spatial arm, which is attached to the body of the mobile robot, carries a nozzle at its end effector. The joint attached to the robot's base, controls the yaw of the nozzle, while the other two revolute joints contribute to the pitching and positioning of the nozzle. The 3-R arm will aid in accessing elevated areas, consequently increasing the workspace.

Inspired by the Thermite Robot, created by Howe x Howe, the design incorporates a high-temperature resistant and fire protection shield that is used to protect the
controllers and back of the robot. The protective shield is made from intumescent materials that expand and become denser when exposed to fire or intense heat [3]. One
of the main goals of creating a fire-fighting robot is its capability to access areas where it is unsafe for firefighters to enter. The robot can be remotely controlled by an operator at a safe distance using lidar, which is placed in a cavity in front of the robot. Even though the robot is controlled remotely, the robot is programmed to protect itself by keeping a 2-meter distance from the center of the hazard.

Lidar stands for Light Detecting And Ranging which is a remote sensing method that utilizes laser pulses to measure the ranges of an object. A recent discovery by the
researchers at the National Institute of Standards and Technology has used the Lidar system to image three-dimensional objects melting in flames [4]. They concluded that this method offers a precise, safe, and compact way to measure structures as they collapse in a fire. The ultimate goal of the robot is to extinguish fires without the intervention of human firefighters with a pressure nozzle on a hydraulic arm.


- How do I add my products to my application?

- Can I smoothly test my purchases?

- How to distinguish Test purchases from Real purchases?

- Will I be charged while testing my purchase flow?

Although there are different payment systems that you may choose to include in your application, this article is only about the native billing system. Also if you have no technical background, that’s ok 🙂. This article is not about how to develop but rather how to configure your billing.

We assume here that you have already developed your InApp Purchase (IAP) process. If that is not the case, I wrote an [Android library](https://github.com/StephenVinouze/KinApp) that can bootstrap your project with it.

Let’s break it down so that you feel comfortable when shipping your product to the store. Now buckle up and let’s get it done 🤓.

---

#### Where it all begins

Since we are using the native payment system, we need to start by logging to your google developer account. You can pilot there your Android application.

Ensure you fill all mandatory fields. It would be right to feel that it looks premature at this step. However, you need a published application to test your IAP.

#### Configure your merchant account

Once your application ready to be published, go to **Store presence > In-app products**. You may need to create a merchant account that allows your company to get paid.

> Be aware that creating merchant account is available to a limited set of countries. Make sure that your company matches this requirement before going any further or you won’t be able to go any further.

#### Add your products

With your merchant account configured you can now create the products that you want to propose to your end-users. There are two distinct types of products:

- Managed products

- Subscriptions

Subscriptions behave a bit differently than In-app products. For the sake of simplicity, we will focus on “managed products”.

Click on ADD NEW PRODUCT and select a product id.

![The product id cannot be changed once created so choose wisely 😉](https://cdn-images-1.medium.com/max/5096/1*eWJhmUAC7rv-_eg2wLD56Q.png)

Fill in the title, description, price and finally activate the product

![We have now two different products available 🤩](https://cdn-images-1.medium.com/max/5108/1*i4r2P852VQ6vm3Uz_RoATQ.png)

You are now ready to test your IAP flow by fetching your In-app products and attempt payment on them.

#### Try it out!

Launch your application and see that you can fetch your products! Now try to make a payment. You will end up with this dreadful error dialogue:

![No can do sir 🧐](https://cdn-images-1.medium.com/max/1124/1*PJulZ3hoBOME8vQnLaOWTg.png)

You will need to build a signed APK in release mode and publish it to the PlayStore. You can either use the alpha or Beta channel to keep the publication private to a set of known users. From the Release management panel, on the App releases section :

![IAP won’t work unless you publish your app either on Alpha or Beta channel 🙄](https://cdn-images-1.medium.com/max/5100/1*datiWD6aUiS0BnaKO_EEmw.png)

Configure your publication and upload your release artifact. Save it and validate it for review.

### The review can take up to a few hours before your application will be published on the PlayStore. Be patient ;)

Remember to manage your Beta-tester list that will be able to download the application once published. Go to **Settings > Manage testers** :

![Manage your testers that can access your IAP products](https://cdn-images-1.medium.com/max/5100/1*_T0JagYvFhxQzFaT2qiHsQ.png)

Any user on this list will receive an invitation to test your application. Before being able to download it (assuming it is published), log in to your Gmail account that is listed in the Beta tester list and go to the following link :

[https://play.google.com/apps/testing/{your.package.name}](https://play.google.com/apps/testing/%7Byour.package.name%7D)

where `{your.package.name}` must be replaced by your application's package name. Accept the invitation. You should now be able to download the application from the PlayStore once validated by Google. You will then be able to process your purchases.

#### Distinguish Test purchases between Real purchases

As soon as your application is available via the store, you can try to purchase your product. Be careful, though, as you are using Real purchases!

You can bypass the payment process by adding your email address in the License testing list.

Do not confuse the License testing list with the Beta tester list. Although it looks similar, they are not located at the same place and have a different purpose :

- Beta tester list allows users to download your Alpha/Beta application submitted on the PlayStore

- License testing list allows users to process IAP without being charged

Go to **Settings > Developer account > Account details**

![Here is where the magic happens 😎](https://cdn-images-1.medium.com/max/5104/1*1IHN0zk4o8ym6Kg83gjJ4g.png)

Go back to your application and re-attempt to buy a product. You should now see a “debug” label disclaiming that this is a test purchase.

![A test payment request from Google PlayStore](https://cdn-images-1.medium.com/max/1372/1*ODK39i6LpcwnNa1buz2Izw.png)

You are now ready to thoroughly test your IAP flow without having to worry about being charged 🤟.
