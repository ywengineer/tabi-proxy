SOCKS5 proxy server for iPhone + Mac OS X zero-configuration agent
===========================
Overview
-----------------------
#Pros (in no particular order)
1. Open source (YAY!)
2. No jailbreak required
3. Cute icon. The moment I saw it I wanted to have an app that proudly carries it
4. Automatic client configuration (Mac OS X only). See Usage section
5. Growl notifications about newly discovered servers, connection, disconnection...
6. Minimalistic user interface in compliance (I'd like to think so) with Apple's guidelines
7. Ability to turn iPhone screen off while operating (cover proximity sensor with something). Saves some juice, you know...
8. Multiple clients can connect the same iPhone and share its internet connection
9. Kept me busy for couple weeks
#Cons
iPhone development license is required
Not real tethering
Probably contains bugs. See Known bugs section. If something goes wrong and agent app exits unexpectedly, launch it again, it'll restore proxy configuration that was before any changes were made
Agent does lots of debugging output onto system console. Necessary evil for time being
#Usage
##Mac OS X
1. Launch Tabi agent. Enter your password when prompted - it's needed for making changes in network preferences. (I wonder what happens if user refuses to enter password - should probably file a bug report for myself...)
<br/>
2. [Create ad-hoc network](http://docs.info.apple.com/article.html?path=Mac/10.5/en/8339.html). I encourage you to password-protect the network

##iPhone
3. Connect to ad-hoc network created on step 2
<br/>
4. Launch Tabi app and wait...

whew... It's up and running. Now, switching attention back to Mac OS X

##Mac OS X
5. If you choose Auto-Connect option, Tabi agent connects to proxy server running on iPhone by itself by changing network preferences:
<br/>
6. If you're curious you can see it for yourself by opening System Preferences -> Network -> Advanced (usually for AirPort interface) -> Proxies:
7. After changes are made agent sends system-wide notification using Growl if available:

#Known bugs
Agent doesn't handle the case when user refuses to enter the password to unlock system preferences
Sometimes Agent doesn't receive notification of shutdown service. Try to turn on/off SOCKS proxy on the iPhone
Non-interesting stuff
Uses [Bonjour](http://developer.apple.com/networking/bonjour/faq.html) for service discovery
[Plausible blocks](http://code.google.com/p/plblocks/) made my life easier. BTW, make sure you have it installed before you compile iPhone application
Side-effect of enabling proximity sensor is ability to turn iPhone's screen off
#Plans
Do something about security. Option to 'connect' client machine to known iPhones only
Show traffic on the iPhone
???
#Credits
Snail icon is made by [jordanfc](http://jordanfc.deviantart.com/art/full-size-snail-icon-150551795)
