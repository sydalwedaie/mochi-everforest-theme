<div align="center">

![](./docs/mochi-everforest-theme.png)

# Everforest Theme for the Mochi.cards App

A beautiful, customizable [Everforest](https://github.com/sainnhe/everforest) color scheme for the [Mochi](https://mochi.cards) flashcard application. This theme provides custom dark and light modes for excellent readability and visual comfort.

<a href="https://buymeacoffee.com/sydalwedaie">![Buy me a coffee badge](https://img.shields.io/badge/Buy_Me_A_Coffee-FFDD00?style=for-the-badge&logo=buy-me-a-coffee&logoColor=black) </a>
</div>

## Features

- Seamless dark and light theme variants in one file.
- Three contrast levels (hard, medium, soft) for both dark and light modes (default medium dark, hard light).
- Optional colorful heading styles (H1-H6).
- Optional custome numbered bullets and indent lines.
- Custom font family and styles for standard and extended markdown syntax.
- Custom inline code blocks.
- Custom keyboard input (`<kbd>`) styling.
- Multi-color highlighted text (`==text==`).
- Enhanced table styling with alternating row colors.
- Opinionated layout fixes for the Grid and Column views.

## Installation

Copy the compiled CSS file to your Mochi custom CSS location:

- Navigate to Mochi's settings
- Find the Custom CSS theme option
- Import `everforest-primary.css`

> Note: You need to redo the above steps every time you update the theme file!

Once installed, the theme automatically adapts to your Mochi dark/light mode setting:

- **Dark Mode**: Activates when Mochi is set to dark theme
- **Light Mode**: Activates when Mochi is set to light theme

No additional configuration is needed for basic usage. If you want to customize the theme, use the SCSS source files (see Customization section below)

## Customize Using SCSS

The theme is built with SCSS and offers a few customization options:

1. **Prerequisites**: [Install SASS](https://sass-lang.com/install)
2. **Edit Settings**: Open `_settings.scss` and modify as desired:
3. **Compile**: Generate the CSS file

```bash
sass --watch src/everforest-primary.scss everforest-primary.css
```

## Customization Options

### Contrast Levels

- **Hard**: Maximum contrast between background and foreground (default for light mode)
- **Medium**: Balanced contrast (default for dark mode)
- **Soft**: Lower contrast for reduced eye strain

### Rainbow Headings

Enable or disable colorful heading styles by setting `custom-rainbow-headings` to `true` or `false`. When enabled, you can customize which color is applied to each heading level (H1-H6) using the `rainbow-colors` list.

Available colors: `red`, `orange`, `yellow`, `green`, `aqua`, `blue`, `purple`

> Note: The default for H1 heading is foreground color.

### Custom Components

- `custom-button-3d` adds a 3D effect on some UI buttons.
- `custom-assets-shadow` adds a subtle shadow arround images and videos, making them pop.
- `custom-ol-bullet` adds rounded custom bullet numbers and indentation lines.
- `custom-highlights` adds 4 different highlight options by mixing markdown's `==`, `_` and `**` syntax.
- `custom-bg-pattern` adds a subtle background dot battern to the main content area.

## File Structure

The main entry point is `everforest-primary.scss`. It imports all the components from the `src/components` directory, which eventually compiles into the output `everforest-primary.css` in the root directory.

```
├── everforest-primary.css                 # Compiled output (ready to use)
└── src
    ├── assets
    │   ├── _colors.scss                   # Everforest colors (all variants)
    │   ├── _settings.scss                 # Custom settings options
    │   └── _tools.scss                    # SASS mixins
    ├── components
    │   ├── _base.scss                     # Base styles for the whole app
    │   ├── _fixes.scss                    # Minor UI fixes
    │   ├── _layout.scss                   # Opinionated layout fixes
    │   ├── _syntax-highlighting.scss      # Everforest syntax highlighting
    │   ├── _typography.scss               # Cards typography styles
    │   └── _variables.scss                # Global variables (light, dark, common)
    └── everforest-primary.scss            # Main entry point

```

## References

- [Original Everforest by sainnhe](https://github.com/sainnhe/everforest)
- [Obsidian Primary Theme](https://primary-theme.github.io/)
- [Mochi Website](https://mochi.cards)
- [Sass Docs](https://sass-lang.com)

## Contributing

Feel free to customize this theme to your preferences! If you create improvements or variants, consider sharing them with the [Mochi community](https://forum.mochi.cards/).

## License

This theme is based on the Everforest color scheme and the Obsidian Primary theme. Please refer to the original repositories for licensing information.
