---
layout: post
title: System Integrity Protection (SIP) In El Capitan
---


A very good move :)

El Capitan restricts all processes, including root processes from writing (creating directories/files, copying binaries etc) to /System, /bin, /usr (excluding /usr/local), and /sbin. This prevents key system directories from being modified even by the root account. 

[https://en.wikipedia.org/wiki/System_Integrity_Protection](https://en.wikipedia.org/wiki/System_Integrity_Protection) – This explains SIP in brief. 

Expect problems on upgrading to El Capitan. All App store products are going to be safe I guess. But the ones being distributed outside of App store; there are chances of at least few of them failing. As an example, if we have installed homebrew services, then potentially they could live in /usr, which is now out of bounds in El Capitan. Therefore, when we upgrade to El Capitan, a migration will be performed (I haven’t seen any documentation which says where Apple is migrating these files to, or are they getting deleted?), moving these items to directories that are allowed, which could break some solutions.

There is a way to disable this feature, though not recommended.

This can be disabled by booting to the Recovery OS and running a new Security Configuration utility to disable it.

Don't disable this.... Save our OS ...

Thanks!