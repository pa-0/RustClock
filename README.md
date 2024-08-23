<div align="center">

![icon](./assets/icon.png) 

# `Rust_Clock` 
[![license](https://img.shields.io/badge/license-MIT-red.svg)](https://github.com/hoothin/RustClock/releases/tag/0.1.5) [![download](https://img.shields.io/github/downloads/hoothin/RustClock/total)](https://github.com/hoothin/RustClock/releases/tag/0.1.5)

Customizable Popup Clock with Countdown and Audible Alert Functions<br>frequency, duration, appearance, and sound configurable

![example](pic.gif)

</div>

## Built with:

<div align="center">
  
[rust](https://github.com/rust-lang/rust) &nbsp;&nbsp;&nbsp;&nbsp; **|** &nbsp;&nbsp;&nbsp;&nbsp; [egui](https://github.com/emilk/egui/) &nbsp;&nbsp;&nbsp;&nbsp; **|** &nbsp;&nbsp;&nbsp;&nbsp; [rodio](https://github.com/RustAudio/rodio) &nbsp;&nbsp;&nbsp;&nbsp; **|** &nbsp;&nbsp;&nbsp;&nbsp; [tray-icon](https://github.com/tauri-apps/tray-icon) &nbsp;&nbsp;&nbsp;&nbsp; **|** &nbsp;&nbsp;&nbsp;&nbsp; [chrono](https://github.com/chronotope/chrono) &nbsp;&nbsp;&nbsp;&nbsp; **|** &nbsp;&nbsp;&nbsp;&nbsp; [rust-ini](https://github.com/zonyitoo/rust-ini)

</div>

## Install

+ [Release](https://github.com/hoothin/RustClock/releases/tag/0.1.5)
+ Homebrew
``` bash
brew install hoothin/rust_clock/rust_clock
```

## Configuration

_Edit the `conf.ini` file that resides in the same folder as the `rust_clock` app._
_Delete `#` to uncomment optional configurations._

### `conf.ini`Settings 
(_TOC_)

1. [time](#time)
2. [sound](#sound)
3. [countdown](#countdown)
4. [pos](#pos)
5. [color](#color)
6. [show_time](#show_time)
7. [tips](#tips)
8. [font_path](#font_path)
9. [bg](#bg)
10. [init_show](#init_show)
11. [timezone](#timezone)
12. [time_font](#time_font)
13. [round](#round)
14. [time_countdown](#time_countdown)

---

+ time
<a id="time"></a>

#### Popup Frequency 
_Set by `hour:minute:second`. Split multi-time by `,`._

```ini
# popup every half hour per clock
time=:30:

# popup every half hour and at the top of every 15:00 hours
time=:30:,15::0
```
+ sound
<a id="sound"></a>

#### Popup Alert Sound File

```ini
# play sound.ogg when popup
sound=sound.ogg

# play assets/1.mp3 when reaches first time you set，play assets/2.mp3 when reaches second time you set.
sound=assets/1.mp3|assets/2.mp3

# Increase the countdown sound effect on the above basis, play assets/3.mp3 when reaches first countdown you set，play assets/4.mp3 when reaches second countdown you set.
sound=assets/1.mp3|assets/2.mp3*assets/3.mp3|assets/4.mp3
```

+ countdown
<a id="countdown"></a>

#### Repeating Countdown Settings 
_Set using `hour:minute:second` syntax. Split multi-time by `,`._

```ini
# 20-20-20 Eye Protection Rule
countdown=:20:,::20
```

+ pos
<a id="pos"></a>

#### Popup Screen Position

```ini
# popup from right side of screen, 20% top of screen height.
pos=right,20%
```
+ color
<a id="color"></a>

#### Clock Color. 
_Format by **`r,g,b`** or **`r,g,b,a`**_

```ini
# Color of background.
bg_color=207,210,206,200

# Color of border.
border_color=91,105,114

# Color of number background.
number_bg_color=235,235,235

# Color of number.
number_color=0,0,0

# Color of clock circle background.
clock_bg_color=235,235,235
```

+ show_time
<a id="show_time"></a>

#### Popup Persistence Duration. 
_Set in milliseconds_

```ini
# Continuous display for 1000 milliseconds after pop-up
show_time=1000
```

+ tips
<a id="tips"></a>

#### Clock Caption Text

```ini
# display 'time for a break' in popup
tips=time for a break
```

+ font_path
<a id="font_path"></a>

#### Font File Path (for Caption Text)
_(`*.tff`)_

```ini
# use font which is located in 'C:/Windows/Fonts/zongyi.TTF'
font_path=C:/Windows/Fonts/zongyi.TTF
```

+ bg
<a id="bg"></a>

#### Background Image File Path
_Sizes: 80\*80 for clock, 320\*100 for total background_

```ini
bg=assets/bg.png
```
+ init_show
<a id="init_show"></a>

#### Show clock after initialization, 0 means disabled, 1 means enabled

```ini
init_show=0
```
+ timezone
<a id="timezone"></a>

#### Timezone of clock, from -12 to +12

```ini
timezone=+9
```
+ time_font
<a id="time_font"></a>

#### Clock Numerical Font File Path (for Styling Numbers)

```ini
time_font=C:/Windows/Fonts/zongyi.TTF

```
+ round
<a id="round"></a>
> Round the corners of frame, 0 means no

```ini
round=0
```
+ time_countdown
<a id="time_countdown"></a>

#### Enable Countdown

```ini
time_countdown=1
```
