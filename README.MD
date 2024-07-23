# ChatTriggers
<div align="center">
  <p>
    <a>
      <img src="https://chattriggers.com/assets/images/logo-final.png" width="546" alt="ChatTriggers.js" />
    </a>
  </p>
</div>

ChatTriggers is always in development. Although we try to follow standard version conventions and deprecate old methods before removing them, there may be times where we need to restructure something to the point where deprecation is impossible. Modules can and will break at any time.

### About
ChatTriggers is a framework for Minecraft that allows for live scripting and client modification
using JavaScript. We provide libraries, wrappers, objects and more to make your life as a modder
as easy as possible. Even without the proper wrapper, you can still use exposed Minecraft methods
and variables but you will need knowledge of FML mappings. The entire ChatTriggers engine is built
on [Rhino](https://developer.mozilla.org/en-US/docs/Mozilla/Projects/Rhino) using Java 8
so you have access to any Rhino methods and functions. Rhino supports _some_ ES6 features,
as can be seen [here](https://mozilla.github.io/rhino/compat/engines.html).

The basic premise of ChatTriggers is that everything is based around Triggers.
From a modding standpoint, Triggers can be thought of as event listeners.
These can range from a chat Trigger that runs on a specific chat event matching criteria to a
render overlay Trigger that runs when the crosshair is being rendered. We are constantly adding
more Triggers and Trigger types as the mod evolves for more integration with Minecraft.

```JavaScript
register("chat", function(name, message, event) {
  cancel(event);
  ChatLib.chat(name + ": " + message);
}).setCriteria("<${name}> ${message}");

register("renderCrosshair", function(event) {
  cancel(event);
  Renderer.drawRect(
    0x50ffffff,
    Renderer.screen.getWidth() / 2 - 1,
    Renderer.screen.getHeight() / 2 - 1,
    2, 2
  );
});
```

### Installation

Download the newest Release and use it like every other forge mod.

### How to install a forge mod
- [Download the latest forge version](http://files.minecraftforge.net/maven/net/minecraftforge/forge/index_1.8.9.html "Download Forge")
- Run it to install forge  

- Open minecraft launcher and check if forge's profile is there, if not then you can create it ![image](https://user-images.githubusercontent.com/74936369/111808098-b8d7bf00-88e4-11eb-8a2d-60e93b1406a5.png)
- **Windows**: Press windows+r and type %appdata%/.minecraft/
- **Linux**: .minecraft is located in your home folder. ~/.minecraft
- **Mac**: do ⌘ (Command) + Space type "~/Library/Application Support/minecraft/
- Create a folder called "mods" if it isnt there already. then put the mods you download inside that folder and start minecraft.
                   
### Legal Disclaimer

This was made for educational purposes only, nobody which directly involved in this project is responsible for any damages caused.
**You are responsible for your actions.**
