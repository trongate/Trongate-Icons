# Trongate Icons

**Version 0.1.1** (Beta)

A lightweight icon set for the Trongate PHP framework. Trongate Icons provides scalable vector icons that work seamlessly with Trongate's existing CSS framework.

## Installation

### Step 1: Download Trongate Icons from GitHub

1. Go to the Trongate Icons GitHub repository
2. Click the green **"Code"** button
3. Select **"Download ZIP"**
4. Extract the downloaded ZIP file to a temporary location on your computer

### Step 2: Copy the CSS File

1. Locate the `trongate-icons.css` file from the extracted folder
2. Copy it to your project's `public/css` directory
3. The file path should be: `your-project/public/css/trongate-icons.css`

### Step 3: Copy the Icons Folder

1. Locate the `trongate-icons` folder (containing the SVG files) from the extracted folder
2. Copy the entire `trongate-icons` folder to your project's `public` directory
3. The folder path should be: `your-project/public/trongate-icons/`
4. Individual icon paths will be: `your-project/public/trongate-icons/user.svg`, `your-project/public/trongate-icons/star.svg`, etc.

### Step 4: Add the Stylesheet to Your Project

In your template or view files, add the following line in the `<head>` section:

```html
<link rel="stylesheet" href="<?= BASE_URL ?>css/trongate-icons.css">
```

**Note:** Ensure `trongate.css` is also loaded, as it provides sizing classes (xl, lg, sm, xs) and effects.

### Step 5: Commit Your Changes (Git - Optional)

If your project is tracked by Git:

```bash
cd /path/to/your-project
git add public/css/trongate-icons.css
git add public/trongate-icons/
git commit -m "Add Trongate Icons"
```

### Step 6: Start Using Icons

You can now use icons in your project:

```html
<i class="tg tg-user"></i>
<i class="tg tg-star"></i>
```

## Quick Start

Using Trongate Icons is simple. Just add an `<i>` tag with the appropriate classes:

```html
<i class="tg tg-star"></i>
```

The basic pattern is:
- `tg` - The base class (required)
- `tg-{icon-name}` - The specific icon you want

## Usage Examples

### Basic Icons

```html
<!-- Star icon -->
<i class="tg tg-star"></i>

<!-- User icon -->
<i class="tg tg-user"></i>
```

### Icons with Sizing

Use Trongate's standard sizing classes:

```html
<i class="tg tg-star xl"></i>  <!-- Extra large -->
<i class="tg tg-star lg"></i>  <!-- Large -->
<i class="tg tg-star"></i>     <!-- Default size -->
<i class="tg tg-star sm"></i>  <!-- Small -->
<i class="tg tg-star xs"></i>  <!-- Extra small -->
```

### Icons in Buttons

```html
<!-- Standard HTML button -->
<button>Click Me <i class="tg tg-star"></i></button>

<!-- Button with icon at the start -->
<button><i class="tg tg-user"></i> Profile</button>

<!-- Icon-only button -->
<button><i class="tg tg-star"></i></button>
```

### Using Trongate Helper Functions

#### With form_button()

```php
// Button with trailing icon
echo form_button('action', 'Save <i class="tg tg-star"></i>');

// Button with leading icon
echo form_button('profile', '<i class="tg tg-user"></i> View Profile');

// Icon button with attributes
echo form_button('favorite', '<i class="tg tg-star"></i>', ['class' => 'btn-icon']);
```

#### With form_submit()

```php
// Submit button with icon
echo form_submit('submit', '<i class="tg tg-star"></i> Submit');

// Submit with sizing
echo form_submit('save', '<i class="tg tg-star lg"></i> Save Changes');
```

### Colored Icons

Icons inherit the text color of their container:

```html
<p style="color: blue;">
    <i class="tg tg-star"></i> Blue star
</p>

<button style="color: red;">
    <i class="tg tg-user"></i> Red user icon
</button>
```

## Available Icons

For a complete list of all available icons, see the [Icon Gallery](../../wiki/Icon-Gallery) or browse the SVG files in the `trongate-icons` folder.

## How It Works

Trongate Icons uses SVG masks for maximum flexibility. Each icon is an SVG file that gets applied as a mask, allowing the icon to inherit colors and scale perfectly at any size.

## Browser Support

Trongate Icons supports all modern browsers:
- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)
- Opera (latest)

## Contributing

Contributions are welcome! If you'd like to suggest new icons or report issues:

1. Check the [issue tracker](../../issues) to see if it's already been reported
2. Open a new issue with a clear description
3. For icon requests, please include use cases and examples

## License

Trongate Icons is released under the [MIT License](LICENSE).

You are free to use this icon set in personal and commercial projects.

## Credits

Created for the [Trongate PHP Framework](https://trongate.io).

---

**Made with ❤️ for the Trongate community**