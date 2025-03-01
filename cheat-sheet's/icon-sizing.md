# Favicon Cheat Sheet
Stolen from: [audrey feldroy](https://github.com/audreyfeldroy/favicon-cheat-sheet). And re-formatted in Markdown.

## The HTML

### Basics

For cross-browser compatibility, use a `favicon.ico` file placed in the root of your domain. This works in all desktop browsers back to IE6, except for SeaMonkey.

### Optional But Encouraged

1. **Touch icon for iOS 2.0+ and Android 2.1+:**
    ```html
    <link rel="apple-touch-icon-precomposed" href="path/to/favicon-180.png">
    ```
2. **IE 10 Metro tile icon:**
    ```html
    <meta name="msapplication-TileColor" content="#FFFFFF">
    <meta name="msapplication-TileImage" content="/path/to/favicon-144.png">
    ```
3. **IE 11 Tile for Windows 8.1 Start Screen:**
    ```html
    <meta name="application-name" content="Name">
    <meta name="msapplication-tooltip" content="Tooltip">
    <meta name="msapplication-config" content="/path/to/ieconfig.xml">
    ```
    **ieconfig.xml:**
    ```xml
    <?xml version="1.0" encoding="utf-8"?>
    <browserconfig>
      <msapplication>
        <tile>
          <square70x70logo src="/path/to/smalltile.png"/>
          <square150x150logo src="/path/to/mediumtile.png"/>
          <wide310x150logo src="/path/to/widetile.png"/>
          <square310x310logo src="/path/to/largetile.png"/>
          <TileColor>#FFFFFF</TileColor>
        </tile>
      </msapplication>
    </browserconfig>
    ```

## The Images

### Minimum Required

| Size       | Name            | Purpose                        |
|------------|----------------|--------------------------------|
| 16x16, 32x32 | favicon.ico    | Default required by IE, Chrome and Safari may pick `.ico` over `.png`. |

### If You Care About iOS and Android

| Size   | Name               | Purpose                            |
|--------|--------------------|------------------------------------|
| 180x180 | favicon-180.png   | General use iOS/Android icon.     |

### If You're Obsessive

| Size   | Name               | Purpose                            |
|--------|--------------------|------------------------------------|
| 32x32  | favicon-32.png     | Fixes Chrome issues.              |
| 57x57  | favicon-57.png     | iPod Touch, iPhone (1st-3rd gen). |
| 76x76  | favicon-76.png     | iPad icon.                        |
| 96x96  | favicon-96.png     | GoogleTV icon.                    |
| 120x120 | favicon-120.png   | iPhone retina touch icon.         |
| 128x128 | favicon-128.png   | Chrome Web Store icon.            |
| 144x144 | favicon-144.png   | IE10 Metro tile.                  |
| 152x152 | favicon-152.png   | iPad retina touch icon.           |
| 196x196 | favicon-196.png   | Chrome for Android.               |

## ICO File

An `.ico` file contains multiple `.bmp` or `.png` icons of different sizes. Recommended sizes:

| Size   | Purpose                                      |
|--------|----------------------------------------------|
| 16x16  | IE9 address bar, Windows taskbar button.   |
| 32x32  | New tab page in IE, Safari sidebar.         |
| 48x48  | Windows site icons.                         |

For the best support, also include:

| Size   | Purpose                                      |
|--------|----------------------------------------------|
| 24x24  | IE9 pinned site browser UI.                 |
| 64x64  | Safari Reading List sidebar in Retina.      |

## SVG File

Safari 9+ uses SVG for pinned tabs. Use a black-only vector with transparency:

```html
<link rel='mask-icon' href='icon.svg' color='#ff0000'>
```

## Helpful Tools

1. **[OptiPNG](http://optipng.sourceforge.net/)** – Optimize `.png` files.
2. **[ImageMagick](http://blog.mrubel.org/blog/2007/09/30/pngs-to-favicons/)** – Create `.ico` from `.png` files.

## License

This cheat sheet is open-source and available under the [MIT License](LICENSE).

