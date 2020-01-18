# Raspberry Pi Ultra-WideSscreen Config
I installed [Libreelec](https://libreelec.tv) on my Raspberry Pi 3B+ and hooked it up to a 34" 2560x1080px ultra-widescreen computer monitor. To deal with this unusual scenario, I had to define a few things in the config.txt file to get it all ticking. It seems to be working nicely so far.

## The settings
Here is the info needed to make it work:
`
# Make display smaller to stop text spilling off the screen
#
# Note that the overscan settings only affect the splash screen and not Kodi.
#
# If you experience overscan/underscan issues the best solution is to adjust
# your TV settings ("full pixel", "1-1 pixel" etc.). Alternatively, there is a
# calibration menu in the Kodi GUI.
#disable_overscan=1

# Force HDMI even if unplugged or powered off
# hdmi_force_hotplug=1

# Doesn't sent initial active source message.
# Avoids bringing CEC (enabled TV) out of standby and channel switch when
# rebooting.
hdmi_ignore_cec_init=1

hdmi_drive=2
hdmi_ignore_edid=0xa5000080
hdmi_group=2
hdmi_mode=87
hdmi_aspect_21_9=7
hdmi_pixel_freq_limit=400000000
hdmi_cvt=2560 1080 60 7 0 0 1
#config_hdmi_boost=8
max_framebuffer_width=2560
max_framebuffer_height=1080
framebuffer_width=2560
framebuffer_height=1080
`
