<!--
Created (20/11/2020) by Paolo-Prete.
This file is part of Spontini-Editor project.

Spontini-Editor is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.
Spontini-Editor is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with Spontini-Editor. If not, see <http://www.gnu.org/licenses/>.
-->

# Miscellaneous
<br></br>

### CAIRO-SVG

If enabled, Spontini-Editor can generate PDF documents of the edited scores.
In order to enable and make it work:

  1. Set **"cairosvg-enabled"** to **"yes"** in **[saved-config.txt](../lib/saved-config.txt)**
  
  2. Uncomment the line containing *"CairoSVG==xxx"* in **[requirements.txt](../lib/python/requirements.txt)**
  
  3. [WINDOWS] Install **[Visual C++ Build Tools](https://visualstudio.microsoft.com/thank-you-downloading-visual-studio/?sku=BuildTools&rel=16)**
  
  4. [WINDOWS] Install **[GTK Runtime Environment](https://github.com/tschoonj/GTK-for-Windows-Runtime-Environment-Installer/releases)**
  
In case of issues, please refer to **[THIS](https://cairosvg.org/documentation/)** link.

Also, before generating the PDF file, make sure that editor's objects are not visibile:

```
#(set! showEditorStuff "false")
```

### DOCK / UNDOCK SCORE BUTTON

... Don't forget to allow popups from Spontini-Editor's URL in your browser: then you can undock/dock the score into/from a separated window by pressing this button.

### EXTRACTING SCORE PARTS

With the following tools:

  * Make all &#95;&#95;BLOCK&#95;&#95;s included
  * Make all &#95;&#95;BLOCK&#95;&#95;s inline
  * Make &#95;&#95;BLOCK&#95;&#95; included
  * Make &#95;&#95;BLOCK&#95;&#95; inline

... parts of the score can be automatically extracted as separate files, or put inline into the main ly file, as **[THIS](../examples/string-quartet-template-example.ly)** example shows.
  
### FORK MODE

By choosing ***FILE ---> FORK***, you can create a copy of the current document, with a random generated name, and make it automatically available on the www for collaborative editing (just copy and share the generated link).

You can run the web-server in **"fork-access-only"** mode as well, which is an option included in **[saved-config.txt](../lib/saved-config.txt)**: if set to **"yes"**, the **"OPEN"** and **"DELETE"** options of the menu will be disabled, so that the forked files won't be seen/deleted by users connected to the same web server's host.

### MIDI VLC PLUGIN

This plugin can be launched on the web server's host. You can enable it by setting the **&lt;enabled&gt;** tag to **"true"**, inside **[plugins.xml](../plugins/plugins.xml)** and installing **[VLC](https://www.videolan.org/vlc/index.html)** with MIDI support. Check **[https://wiki.videolan.org/Midi/](https://wiki.videolan.org/Midi)** for more infos.

A minimal skin, which is good for a MIDI player (it doesn't show the default video panel) is included into the plugins directory (mpui.vlt): you can set it by following **[THESE](https://www.videolan.org/vlc/skins.html)** instructions.

### MOBILE DEVICES

If, for some reasons, you use a mouse with your mobile device but the right button doesn't work, try to launch the client with the following URL:

```
http://localhost:8000/spontini-editor?mobilemode=yes
```

Then the svg drop-down menu is displayed after a double click on the left mouse button.

### OUTPUT

You can check the LilyPond compiling output in two ways:

  * On the Javascript console of your browser (open "Web developer" ---> "Web console" on Firefox and "More tools" ---> "Developer tools" on Chrome/Chromium).
  * On the Spontini-Server's window or on the Spontini-Server's output (if the server is launched with "nogui" option)
  
### PAN-ZOOM

You can activate it by pressing the len button on the menu, or by keeping **CTRL** key pressed. Use the mouse wheel and/or zoom-in/out by using the left mouse button and the keys listed inside **[global-custom-vars.js](../lib/webgui/js/global-custom-vars.js)**.
Note that you can't do point and click, nor edit the svg score while panning/zooming.

### TOUCHPAD

Spontini-Editor works with touchpads too: simply use a double tap (you can test it **[HERE](https://rbyers.github.io/paint.html)**) instead of the mouse down action and a two-fingers double tap instead of the right mouse button action.

### [TABLE OF CONTENTS](toc.md)
