---
layout: post
title: "DIY BlackPhone"
description: "Re-Configuring an Android Phone for Security"
category:
tags: [Security]
---
{% include JB/setup %}

As part of my recent "secure my life" commitment, I went through the process of re-configuring my Android Nexus 4 into a secure-as-possible smartphone very similar to the [BlackPhone concept](https://www.blackphone.ch).

Going into this process I had a few goals:

- minimize the likelihood of backdoor in the source or apps.
    - [Cyanogenmod](https://www.cyanogenmod.org/)

- minimize my traceability via my cellphone by other parties
    - nothing...

- secure as much as traffic coming in and out of the phone as possible
    - VPN is broken for constant use

- anonymized as much of the network traffic as possible
    - [TOR](https://www.torproject.org/)
    - [OrBot](https://www.torproject.org/docs/android.html.en)

- Setup PGP for email on my phone
    - [APG](https://play.google.com/store/apps/details?id=org.thialfihar.android.apg)
    - [K9-Mail](https://play.google.com/store/apps/details?id=com.fsck.k9)

- Setup as much protection for my IM communication as possible
    - [TextSecure and RedPhone](https://whispersystems.org/)
    - [ChatSecure](https://chatsecure.org/)

## Backdoors

When it comes to minimizing software back-doors we are limited in options.
I've decided the best approach to minimizing backdoors is to install Cyanogen mod on my Nexus 4. There are fundamental limits to how much I can do to prevent backdoors at the operating system level (or hardware level for the matter) so I am taking the "many eyes" approach and using as much open source software as possible.
Cyanogen tends to be a release point behind mainline android, but Kit-Kat did not have any features I was really excited about.

Installing cyanogen was actually pretty easy (after I stopped making it hard by not following the directions) The only difficult part is that the installation directions assumed I used a UNIX based operating system. I am currently using windows on my personal computers so there was a bit of an adventure making sure my path variables were right and I used the right commands.

## Tracking

Minimizing my trackability is also a losing battle. When Booting Cyanogen mod for the first time, if you chose to attach it to a Google or Cyanogen account you can choose to disable sending those services your location. If you feel extra paranoid you can disable your GPS in the location settings menu. Even with all of this, the cell network has to track your location to a certain degree simply so they can give you service.

## Network Security

Securing traffic is actually one of the harder parts of this challenge. The ideal solution is a VPN and Android has a VPN client built in. However the "always on VPN" feature which is intended to ensure all network traffic goes over your VPN has been [broken](https://code.google.com/p/android/issues/detail?id=53451) since its introduction as a feature. Here the Android TOR client shines as an overkill solution. OrBot requires you to have rooted your phone (this far along that is not much of an issue) and can redirect all or a subset of traffic via the TOR network. This also fulfills our goal of anonymizing as much traffic as possible.


## Pretty Good Privacy

PGP proved easy to setup. APG acts as a good PGP service for android. You can generate new keys with it or import subkeys from your computer to authenticate your emails. K9-mail works well and integrates with APG. Now all my email from my phone is signed, and I can decrypt and verify messages (and sign and encrypt!) The only fiddly bits of K9-mail are that it auto-enables a self-advertising signature on all your outgoing email you need to disable.

## Texts, IMs and Voice

Text secure has had a lot of interesting advances lately: TextSecure and Redphone from WisperLabs look like good tools for securing phone to phone communications. TextSecure has the interesting feature, that while keys are being exchanged between phones via TextSecure's servers, it would be very difficult for them to intercept and MITM our text messages.

Finally, I want to use OTR encryption for as many chat services as I can. ChatSecure, which integrates with OrBot, seems to be the most straightforward client.

## Conclusions

It is certainly possible to secure your phone. The real issue is that communications security only works when both parties use it. Worse, tools like TextSecure and Redphone are the best we have for now, but in the long run there is no trusted third party for key exchange.

Note there are security concerns I did not address here, notably how to encrypt the contents of your phone (luckily this is now an android feature) [this](https://www.encrypteverything.ca/index.php?title=Cell_phone_privacy_guide_(Android)) looks like a good through guide for local security.
