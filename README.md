# Miiverse Design Guide
Welcome to the Miiverse Design Guide! This guide teaches you how to make 3DS-era, Miiverse-like applications in any UI library.

## Backgrounds
There are two ways to make your background Miiverse-like. You can either use [this image](data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAPAAAADwBAMAAADMe/ShAAAAHlBMVEX29vb09PTy8vL19fXz8/Px8fHw8PDv7+/u7u739/dHdNvrAAACSElEQVR4AezYNX7DMBiGcafcKTRlC0hdy7T1Z7iAcS5YOkEl38DeQlNOW24YX63fsxr+Ztm2RmvjMiu2bWbOXPmjtW2A7S8YKlfMCK4lKPzeMoJvYhROHYIJno9gggkmmGCCCSaYYIIJJphgggkmGP/PZQZf4XDHCK5JFFYtE7hXkwWYap0awEMPh8NHA7jPNQprv2EAH5zh8MsTDo9vY/xGxuCeLXFYsVMY7nNZwCm/AcM3scZhnTooPBwfafBYP4JwiZvBfgWDh7Xxkc71DmXjY916hOAbLrMxK7ZuTOfKdxC4ZMf6z1Ui2iEh/2Sdssru8L4dy+zXFVGbuVtntyPxK+cqZRc7wr1Ll0v95/qser1DVZv/yVr5bv10Bczq+ML4Rl/als/ww4WfJptbwuACMbgwhaUVfkvgt6LU1icpdkAAAADAEEz/1EKshHOBgMAnwZ7gNgG9DEwybTKpyZiLRCT6ItqUCJuIYqKoosaJlEsMJBki+ZOElwRfkpqSuElcS9Qnd4LcGN3enRUACMRQDFSDJRzg3wIKuNnNzygYA83rGbx9g1cwGAwGg8FgMBgMBoPBYDAYDAaDwWAwGAwGg8FgMBgMBoPB/bFgfx7ZH4TWJ7DB0W9w5hwcdgen7MHxfp8r9IFGkKQEEU6WHWWhVZaWZTFdlg9mwWSdiAZRbJABB+FzkHoHcXuQ82cDBtlkQzVSkc1yZEMk2fRKNjZTzetkg0LlhJK1KjAYDAaDwWAwGAwGg8FgcAD3L/H6J4DLS/j67eEOl9GYoKbAV2YAAAAASUVORK5CYII=) repeating at a small scale or simply set the background to <b>#eeeeee</b>.

## Text
Use a text colour of <b>#606060</b>, and the font nintendo_NTLGDB_001 ([ttf](/nintendo_NTLGDB_001.ttf) or [woff](/nintendo_NTLGDB_001.woff)).

## Buttons
You can use a button coloured <b>#5ac800</b> with a border radius as high as it will go. With a font size of 12, having the button 24px tall looks good. The border width should be 0px and the font colour should be <b>#f4f4f4</b>.
<br><br>
Some example CSS to achieve this is:
```
button {
    font-family: nintendo_NTLGDB_001;
    background-color: #5ac800;
    color: #f4f4f4;
    border-radius: 12px;
    height: 24px;
    border: none;
}
```
which produces:
<iframe src="/button-example.html"></iframe>

</html>

### Alternate White Button
This button may end up being the most common style of button in your app. This button has the background colour <b>#ffffff</b> and text colour <b>#323232</b> with a drop shadow straight downwards.
<br><br>
Some example CSS to achieve this is:
```
button {
    font-family: 'nintendo_NTLGDB_001';
    background: #fff;
    border: 1px solid rgba(0, 0, 0, 0.1);
    overflow: hidden;
    box-shadow: 0 1px 0px rgba(0, 0, 0, 0.2);
    border-radius: 5px;
    text-align: left;
    color: #323232;
            }
```
which produces:
<iframe src="/button2-example.html"></iframe>

<br>
This design can be implemented into many sizes, types and contents of element, from buttons to scrollable textboxes! Like this: <br>

```
button {
    font-family: 'nintendo_NTLGDB_001';
    background: #fff;
    border: 1px solid rgba(0, 0, 0, 0.1);
    overflow: scroll;
    box-shadow: 0 1px 0px rgba(0, 0, 0, 0.2);
    border-radius: 5px;
    text-align: left;
    color: #323232;
    max-width: 192px;
    max-height: 192px;
}
```

<br>

<iframe src="/button2-example2.html"></iframe>

<br>Remember to set ```overflow: scroll;``` and a max-width and max-height.

## Images

You can put images into boxes with captions. You can do it in CSS like this:

```
            img {
                font-family: 'nintendo_NTLGDB_001';
                background: #fff;
                border: 1px solid rgba(0, 0, 0, 0.1);
                overflow: scroll;
                box-shadow: 0 1px 0px rgba(0, 0, 0, 0.2);
                border-radius: 5px;
                text-align: left;
                color: #323232;
                max-width: 192px;
                max-height: 192px;
            }

            p {
                font-family: 'nintendo_NTLGDB_001';
                color: #969696;
                display: block;
                overflow: hidden;
                white-space: nowrap;
                text-overflow: ellipsis;
                word-wrap: normal;
                margin: 4px;
            }

            div {
                background: #f9f9f9;
                border: 1px solid rgba(0, 0, 0, 0.1);
                overflow: hidden;
                box-shadow: 0 1px 0px rgba(0, 0, 0, 0.2);
                border-radius: 5px;
                width: fit-content;
            }
```
<br>
with the accompanying HTML:

```
<div>
    <img src="test.png"></img>
    <p>Text</p>
</div>
```

<br>

which results in:

<iframe src="/image-example.html"></iframe>

## Text Input

Making a text input is simple. It's a white box with a 3px #e0e0e0 border. Simple. CSS:

```
input {
    font-family: 'nintendo_NTLGDB_001';
    margin: 0 0 15px;
    text-align: left;
    background: #fff;
    border: 3px solid #e0e0e0;
    width: 100%;
    border-radius: 5px;
    box-sizing: border-box;
    color: #323232;
}
```

<iframe src="/textbox-example.html"></iframe>

## Credits
- Nintendo (for Miiverse and the 3DS system font)
- Project Rosé (for inspiration on implementation)
- Mojang (for image of Minecraft)
