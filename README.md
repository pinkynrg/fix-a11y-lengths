<!-- ⚠️ This README has been generated from the file(s) "blueprint.md" ⚠️-->

[![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/colored.png)](#css-unit-transformer-utility---px-rem-optimizer)

# ➤ CSS Unit Transformer Utility - px-rem-optimizer

This utility provides functions for transforming CSS unit values (e.g., `px`, `rem`) within CSS files or property values based on configurable rules. It includes support for rounding, custom length-matching rules, handling complex CSS properties, and replacing hard-coded lengths with CSS/SCSS variables.


[![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/colored.png)](#features)

## ➤ Features

- **Unit conversion**: Transform values between `px` and `rem` or other units.
- **Custom rules**: Define your own matching rules for CSS units.
- **Flexible configuration**: Supports rounding options and custom size mappings.
- **Replace hard-coded lengths**: Replace fixed-length values with CSS/SCSS variables.
- **Complex value transformation**: Handle and transform CSS properties with multiple length values.
- **Preserve formatting**: Retains the original formatting, including spaces, newlines, and comments, in your CSS.


[![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/colored.png)](#configuration)

## ➤ Configuration

The configuration is defined in a `.px-rem-optimizer` file. The schema for the configuration is validated using **AJV**.

### Example `.px-rem-optimizer`:

```json
{
  "baseFontSize": 16,
  "targetPath": ".",
  "excludePaths": ["node_modules", "dist"],
  "round": {
    "enabled": true,
    "roundUpOnTie": true
  },
  "lengthMatchingRules": {
    "px": "(-?\\d+(\\.\\d+)?|\\.\\d+)px",
    "rem": "(-?\\d+(\\.\\d+)?|\\.\\d+)rem"
  },
  "properties": {
    "width": "rem",
    "min-width": "rem",
    "max-width": "rem",
    "height": "rem",
    "min-height": "rem",
    "max-height": "rem",
    "padding": "px",
    "padding-top": "px",
    "padding-right": "px",
    "padding-bottom": "px",
    "padding-left": "px",
    "margin": "px",
    "margin-top": "px",
    "margin-right": "px",
    "margin-bottom": "px",
    "margin-left": "px",
    "border": "px",
    "border-top": "px",
    "border-right": "px",
    "border-bottom": "px",
    "border-left": "px",
    "border-width": "px",
    "border-radius": "px",
    "outline": "px",
    "outline-width": "px",
    "box-shadow": "px",
    "text-shadow": "px",
    "font-size": "px",
    "line-height": "rem",
    "letter-spacing": "rem",
    "word-spacing": "rem",
    "text-indent": "rem",
    "flex-basis": "rem",
    "gap": "rem",
    "column-gap": "rem",
    "row-gap": "rem",
    "grid-template-columns": "rem",
    "grid-template-rows": "rem",
    "grid-auto-columns": "rem",
    "grid-auto-rows": "rem",
    "background-position": "px",
    "background-size": "px",
    "border-spacing": "px",
    "translate": "rem",
    "translateX": "rem",
    "translateY": "rem",
    "perspective": "rem",
    "transform-origin": "rem",
    "list-style-position": "rem",
    "list-style-image": "rem",
    "clip-path": "rem",
    "mask-position": "px",
    "mask-size": "px",
    "object-position": "rem",
    "scroll-margin": "rem",
    "scroll-margin-top": "rem",
    "scroll-margin-right": "rem",
    "scroll-margin-bottom": "rem",
    "scroll-margin-left": "rem",
    "scroll-padding": "rem",
    "scroll-padding-top": "rem",
    "scroll-padding-right": "rem",
    "scroll-padding-bottom": "rem",
    "scroll-padding-left": "rem",
    "shape-margin": "rem",
    "stroke-width": "px",
    "column-rule": "px",
    "cursor": "px"
  },
  "sizes": {
    "0": {"px": null, "rem": null},
    "1": {"px": null, "rem": null},
    "2": {"px": null, "rem": null},
    "4": {"px": null, "rem": null},
    "8": {"px": null, "rem": null},
    "12": {"px": null, "rem": null},
    "16": {"px": null, "rem": null},
    "20": {"px": null, "rem": null},
    "24": {"px": null, "rem": null},
    "28": {"px": null, "rem": null},
    "32": {"px": null, "rem": null},
    "36": {"px": null, "rem": null},
    "40": {"px": null, "rem": null},
    "44": {"px": null, "rem": null},
    "48": {"px": null, "rem": null},
    "64": {"px": null, "rem": null},
    "80": {"px": null, "rem": null},
    "96": {"px": null, "rem": null},
    "128": {"px": null, "rem": null}
  }
}
```

In the `sizes` section, you can define mappings from hard-coded lengths to CSS/SCSS variables. When the utility transforms the file, it will replace any matching length with the corresponding variable.


[![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/colored.png)](#usage)

## ➤ Usage

No installation is required. You can run the utility directly using `npx`. Simply place your `.px-rem-optimizer` file in the same folder where you are executing the command, and the utility will use it as the configuration.

### Example Command

```bash
npx px-rem-optimizer@latest [file|folder]
```

Replace `[file|folder]` with the path to the CSS file or folder you want to transform.


[![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/colored.png)](#contributing)

## ➤ Contributing

Feel free to open issues or submit pull requests for enhancements and bug fixes.


[![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/colored.png)](#license)

## ➤ License

MIT License
