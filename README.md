# pugl_x11.c.patch
Pugl background transparency example for LV2 plugins with X11

In order to obtain no window border and no black opaque background for openGL 3d plugins like x42 Balance and setBfree, which are uses Pugl, I've created this patch. Tested with `pugl_x11.c` from Balance. As it was considered weird looking by experienced people, I'll not continue this work. However it can gain more success for flat (2d) openGL plugins.

Tested with Ardour, Jalv, and Carla, with X11 & Xfce. Not tested with Wayland.

Add `-lXrender` to both compiler and linker at `Makefile`.

