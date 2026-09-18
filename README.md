# Simple LaunchPad 🚀

![WordPress Plugin](https://img.shields.io/badge/WordPress-Plugin-blue.svg)
![Version](https://img.shields.io/badge/version-3.1.6-green.svg)
![License](https://img.shields.io/badge/license-GPL--2.0%2B-blue.svg)
![WCAG](https://img.shields.io/badge/WCAG-2.1%20AA-success.svg)
![PHP](https://img.shields.io/badge/PHP-7.4%2B-purple.svg)
![WordPress](https://img.shields.io/badge/WordPress-5.0%2B-0073aa.svg)

---

![Simple LaunchPad Banner](https://github.com/rafael-minuesa/Simple-Launchpad/blob/main/.wordpress-org/banner-1544x500.png)

> Simple streamlined command center with quick-access buttons to all WP admin areas.

## ✨ Features

- **🎯 Quick Access** - One-click buttons to all WordPress admin areas
- **🎨 Full Customization** - Colors, ordering, and visibility controls
- **👥 Role-Based Access** - Control which users see which buttons
- **📱 Fully Responsive** - Works beautifully on mobile, tablet, and desktop
- **🌙 Dark Mode** - Automatic dark mode support
- **⚡ Performance** - Lightweight with optimized code
- **🔧 Developer Friendly** - Extensible with filters and hooks
- **🌍 Translation Ready** - i18n compatible

## 📸 Screenshots

Coming soon! Screenshots will show:
1. Dashboard view with quick-access buttons
2. Settings page with drag-and-drop interface
3. Color customization options
4. Role visibility controls
5. Mobile responsive view

## 🚀 Quick Start

### Installation

1. Download the latest release
2. Upload to `/wp-content/plugins/simple-launchpad/`
3. Activate through the 'Plugins' menu in WordPress
4. Go to **Settings → Simple LaunchPad** to configure

### Basic Usage

1. Enable/disable buttons you want to see
2. Drag to reorder buttons
3. Customize colors in the Appearance tab
4. Configure role visibility (optional)
5. Visit your Launchpad!

## 🎨 Customization

### Available Buttons (Default)

- Posts
- Add New Post
- Pages
- Add New Page
- Media
- Comments
- Appearance
- Plugins
- Users
- Settings

### Color Customization

Customize 4 color properties:
- Button text color
- Button hover text color
- Button background color
- Button hover background color

### Role-Based Visibility

Control which WordPress roles can see each button:
- Administrator
- Editor
- Author
- Contributor
- Subscriber
- Custom roles (added by other plugins)

## 🔧 Developer Documentation

### Filter Hooks

#### Add Custom Buttons

```php
add_filter('simple_launchpad_default_buttons', function($buttons) {
    $buttons['my_custom'] = array(
        'label' => __('Custom Area', 'my-plugin'),
        'url' => 'admin.php?page=my-custom-page',
        'icon' => 'dashicons-admin-generic',
        'capability' => 'manage_options'
    );
    return $buttons;
});
```

#### Modify Buttons Before Rendering

```php
add_filter('simple_launchpad_buttons', function($buttons) {
    // Modify the buttons array before it's displayed
    return $buttons;
});
```

### Button Structure

Each button requires these properties:

```php
array(
    'label' => 'Button Label',        // Translatable string
    'url' => 'edit.php',              // Admin URL (relative)
    'icon' => 'dashicons-admin-post', // Dashicons class
    'capability' => 'edit_posts'      // Required capability
)
```

### Available Dashicons

Use any [WordPress Dashicons](https://developer.wordpress.org/resource/dashicons/):
- `dashicons-admin-post`
- `dashicons-admin-page`
- `dashicons-admin-media`
- `dashicons-admin-comments`
- And 300+ more!

## 📊 Performance

Simple Launchpad is optimized for performance:

- ✅ Assets only load on settings pages
- ✅ Minimal database queries
- ✅ No external dependencies
- ✅ Clean, efficient code
- ✅ Follows WordPress best practices

## 🧪 Testing

### Run PHPUnit Tests

```bash
# Install dependencies
composer install

# Run test suite
./vendor/bin/phpunit

# Run with coverage
./vendor/bin/phpunit --coverage-html coverage/
```

### Manual Testing Checklist

- [ ] Enable/disable buttons
- [ ] Drag-and-drop reordering
- [ ] Color picker functionality
- [ ] Role visibility controls
- [ ] Mobile responsiveness
- [ ] Dark mode support
- [ ] AJAX save functionality

## 🤝 Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

### Development Setup

```bash
# Clone the repository
git clone https://github.com/rafael-minuesa/Simple-Launchpad.git

# Install dependencies
composer install
npm install

# Run tests
composer test

# Check coding standards
composer phpcs
```

### Coding Standards

This plugin follows:
- [WordPress Coding Standards](https://developer.wordpress.org/coding-standards/wordpress-coding-standards/)
- [WordPress PHP Documentation Standards](https://developer.wordpress.org/coding-standards/inline-documentation-standards/php/)

## 📋 Requirements

- **WordPress:** 5.0 or higher
- **PHP:** 7.4 or higher
- **MySQL:** 5.6 or higher

## 📝 License

Simple Launchpad is licensed under the [GNU General Public License v2.0 or later](LICENSE).

## 👨‍💻 Author

**Rafael Minuesa**
- Website: [prowoos.com](https://prowoos.com)
- GitHub: [@rafael-minuesa](https://github.com/rafael-minuesa)

## 📞 Support

- **Issues:** [GitHub Issues](https://github.com/rafael-minuesa/Simple-Launchpad/issues)
- **WordPress Support:** [WordPress.org Forum](https://wordpress.org/support/plugin/simple-launchpad/)
- **Documentation:** [Wiki](https://github.com/rafael-minuesa/Simple-Launchpad/wiki)

## 🗺️ Roadmap

See [CHANGELOG.md](CHANGELOG.md) for version history and planned features.

### Future Plans (v2.0+)
- Button analytics
- Quick actions
- Button grouping
- Multi-dashboard support

## ⭐ Show Your Support

If you find this plugin helpful:
- Give it a ⭐ on GitHub
- Rate it on [WordPress.org](https://wordpress.org/plugins/simple-launchpad/)
- Share it with other WordPress users
- Contribute code or translations

---

**Made with ❤️ for the WordPress Community**
