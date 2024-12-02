// in config.h:  
#define POINTING_DEVICE_AUTO_MOUSE_ENABLE  
// only required if not setting mouse layer elsewhere  
#define AUTO_MOUSE_DEFAULT_LAYER 1    


// in keymap.c:  
void pointing_device_init_user(void) {  
    set_auto_mouse_layer(1); // only required if AUTO_MOUSE_DEFAULT_LAYER is not set to index of <mouse_layer>  
    set_auto_mouse_enable(true);         // always required before the auto mouse feature will work  
}  


https://docs.qmk.fm/features/pointing_device#pointing-device-auto-mouse  
https://mazcon.hatenablog.com/entry/2023/11/10/080000  

How to enable:

// in config.h:
#define POINTING_DEVICE_AUTO_MOUSE_ENABLE
// only required if not setting mouse layer elsewhere
#define AUTO_MOUSE_DEFAULT_LAYER <index of your mouse layer>

// in keymap.c:
void pointing_device_init_user(void) {
    set_auto_mouse_layer(<mouse_layer>); // only required if AUTO_MOUSE_DEFAULT_LAYER is not set to index of <mouse_layer>
    set_auto_mouse_enable(true);         // always required before the auto mouse feature will work
}