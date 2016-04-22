---
layout: post
title: Useful Linux/OSX Commands
---


This is a collection from web. Something that I need in my day-to-day life

**User Management**

- groups - Lists all groups to which current/logged-in user belongs to
- dseditgroup -o read &lt;group name&gt; - Lists all info about a group. Useful if you need to know all members of a group
- members () { dscl . -list /Users | while read user; do printf "$user "; dsmemberutil checkmembership -U "$user" -G "$*"; done | grep "is a member" | cut -d " " -f 1; }; 

Usage : members &lt;groupname&gt; - list all users in a group

**CodeSign Validations**

- codesign -v &lt;app/exec name&gt;
- spctl -a -t exec -vv &lt;app/e- xec name&gt;