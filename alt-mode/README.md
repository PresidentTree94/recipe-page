# Instructions for Light/Dark Mode
These are the instructions for how to use Light/Dark Mode in a project. The script creates a SVG, `MOON_ICON` or `SUN_ICON`, and uses it to initialize the `#toggle` button. The default SVG is determined by the value set in the `data-default` attribute. The user can select the button to toggle the mode, which toggles `.altMode` on `body`, and the mode is saved in local storage to persist.

## Requirements
- The "alt-mode" folder and all its contents:
  - toggle-style.css
  - toggle.js

## Steps
1. Add a `<link>` to the HTML to the path of `toggle-style.css`, under the initial stylesheet.
2. Add a `<script>` to the HTML to the path of `toggle.js`, preferably below the stylesheets for organization.
3. Add `<div id="toggle"></div>` to the HTML, where it can be placed in the top-right of the page.
4. Add a `data-default` attribute to `#toggle`, and set it to "sun" or "moon."
5. Assign colors to `#toggle` and the `svg` in the CSS.
6. Add `.altMode` to the CSS and redefine the CSS color variables.
7. Add `.disable-transitions *:not(#toggle) { transition: none !important; }` to the CSS if transitions conflict during mode switches.