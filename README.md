# What is Manokwari?

Manokwari is desktop shell for GNOME3 with GTK+ and HTML5 frontend. Used by BlankOn Linux.

# This script

This slackbuild is **unofficial**, either from Slackware or BlankOn. I only test on slackware64-current (last update June 12, 2018). The developer ship 2 build methods : autotools and meson. This script use meson.

# Dependencies

There are many dependencies that have been already in current and available on [SBo](http://slackbuilds.org). 

1. meson (>= 0.37). Satisfied 
2. glib2 (>= 2.12.0). Satisfied
3. gtk+3 (>= 3.0.8). Satisfied
4. atk (>= 2.0.0). Satisfied
5. vala (>= 1.0.0). Available on SBo vala-0.34.9
6. gee1 (>= 0.6.1). Available on SBo libgee1-0.6.8)
7. cairo (>= 1.10.2). Satisfied
8. gnome-common. Available on SBo gnome-common-3.18.0
9. libgnomemenu (>= 2.30.5). Available on SBo gnome-menus-3.13.3
10. libwnck3 (>= 3.0.0). Available on SBo libwnck3-3.20.1
11. unique3 (>= 3.0.0). Available on SBo libunique3-3.0.2
12. libwebp. 
13. geoclue2. Available on SBo geoclue2-2.4.7
14. webkitgtk (>= 1.3.0). Available on SBo webkitgtk-2.4.11. But if we use from SBo error because libwebkitgtk-3.0.so need libicui18.so.56, libicuuc.so.56, libicudata.so.56, and libwebp.so.5. Slackware64-current now have higher version. Alternative 1 : I built webkitgtk3-2.20.3. Alternative 2 : built new icu4c and libwebp to the suitable version. Alternative 1 may take a long time, so I do the 2nd alternative.  
15. x11 (>= 1.6.0). Satisfied
16. libnotify (>= 0.7.6). Satisfied
17. hyphen. Available on SBo hyphen-2.8.8
18. brotli. Available on SBo brotli-1.0.4
19. woff2. Available on SBo woff2-1.0.2
20. icu4c56.

# Problem

This script build manokwari **without** gnome-session and gnome-desktop. So it's has problems, such as lack of user interface, can't lock the screen, logout, shutdown, reboot, and other problems.  
