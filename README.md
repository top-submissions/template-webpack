# Template Webpack

[![Issues](https://img.shields.io/github/issues/top-submissions/template-webpack.svg)](https://github.com/top-submissions/template-webpack/issues)
[![Pull Requests](https://img.shields.io/github/issues-pr/top-submissions/template-webpack.svg)](https://github.com/top-submissions/template-webpack/pulls)
[![Last Commit](https://img.shields.io/github/last-commit/top-submissions/template-webpack.svg)](https://github.com/top-submissions/template-webpack/commits)
[![Contributors](https://img.shields.io/github/contributors/top-submissions/template-webpack.svg)](https://github.com/top-submissions/template-webpack/graphs/contributors)
[![Downloads](https://img.shields.io/github/downloads/top-submissions/template-webpack/total)](https://github.com/top-submissions/template-webpack/releases)

A production-ready Webpack 5 template repository for modern web development projects. This template provides a complete, pre-configured setup with development and production environments, perfect for quickly starting new JavaScript projects.

## 🚀 Features

- ⚡ **Webpack 5** - Latest bundler with optimal performance
- 🔧 **Split Configurations** - Separate dev and production configs using webpack-merge
- 🎨 **CSS Support** - Style-loader and CSS-loader pre-configured
- 🖼️ **Asset Management** - Image and HTML handling built-in
- 📦 **Module System** - ES6 modules with organized structure
- 🔄 **Hot Reload** - webpack-dev-server with live reloading
- 📅 **Date Utilities** - date-fns library included for date manipulation
- 🏗️ **Project Structure** - Clean, modular folder organization
- 📝 **Documentation** - Complete setup and deployment guide included
- 🎯 **Template Repository** - One-click project creation

## 📋 Prerequisites

Before you begin, ensure you have the following installed:

- **Node.js** (v14.0.0 or higher)
- **npm** (v6.0.0 or higher)
- A modern web browser
- Git for version control

## 🔧 Quick Start

### 1. Use This Template

Click the "Use this template" button at the top of the repository to create a new project, or clone it directly:

```bash
git clone https://github.com/top-submissions/template-webpack.git your-project-name
cd your-project-name
```

### 2. Install Dependencies

```bash
npm install
```

### 3. Start Development Server

```bash
npm run dev
```

The application will open automatically at `http://localhost:8080`

### 4. Build for Production

```bash
npm run build
```

Production-optimized files will be generated in the `dist/` directory.

## 📜 Available Scripts

| Script              | Description                              |
| ------------------- | ---------------------------------------- |
| `npm run dev`       | Start development server with hot reload |
| `npm run watch`     | Watch mode - rebuilds on file changes    |
| `npm run build`     | Create production build                  |
| `npm run build:dev` | Create development build for debugging   |

## ⚙️ Configuration

### Webpack Common (webpack.common.js)

Shared configuration used by both development and production builds:

- Entry point configuration
- Output settings
- HTML plugin setup
- Module rules for CSS, HTML, and images

### Webpack Development (webpack.dev.js)

Development-specific configuration:

- Development mode
- Source maps (`eval-source-map`)
- webpack-dev-server settings
- Hot module replacement

### Webpack Production (webpack.prod.js)

Production-specific configuration:

- Production mode optimizations
- Source maps for production debugging
- Code minification and tree shaking

## 🎨 Styling

The template includes pre-configured CSS support:

- Import CSS files directly in JavaScript modules
- Styles are automatically injected into the page
- Support for modern CSS features

```javascript
// Example: Import CSS in your JavaScript
import './styles.css';
```

## 📦 Module System

Organize your code using ES6 modules:

```javascript
// src/modules/example.js
export function exampleFunction() {
  return "Hello from module!";
}

// src/index.js
import { exampleFunction } from './modules/example.js';
```

## 📅 Date Handling

The template includes [date-fns](https://date-fns.org/) for powerful date manipulation:

```javascript
import { format, parseISO } from 'date-fns';

const date = parseISO('2025-01-15');
const formatted = format(date, 'MMMM dd, yyyy');
```

## 🖼️ Asset Management

### Images

- **In CSS**: Reference images using relative paths - handled automatically
- **In HTML**: Use html-loader to process image paths
- **In JavaScript**: Import images directly

```javascript
import myImage from './images/photo.jpg';
const img = document.createElement('img');
img.src = myImage;
```

## 🌐 Browser Support

- Chrome (latest 2 versions)
- Firefox (latest 2 versions)
- Safari (latest 2 versions)
- Edge (latest 2 versions)

## 📖 Documentation

Detailed documentation is available in the `docs/` directory:

- **[Setup Guide](./docs/SETUP.md)** - Complete setup and deployment instructions
- **Configuration** - Webpack configuration details
- **Best Practices** - Recommended development patterns

## 🚀 Deployment

### GitHub Pages

1. Build the project:

   ```bash
   npm run build
   ```

2. Deploy the `dist/` folder to your hosting service

For detailed deployment instructions, see the [Setup Guide](./docs/SETUP.md).

### Other Platforms

The `dist/` folder contains all files needed for deployment:

- **Netlify**: Drag and drop `dist/` folder
- **Vercel**: Import repository or deploy `dist/`
- **Custom Server**: Upload contents of `dist/`

## 🛠️ Customization

### Add New Dependencies

```bash
npm install package-name
```

### Add New Webpack Loaders

Edit the appropriate webpack config file:

- Common features → `webpack.common.js`
- Development only → `webpack.dev.js`
- Production only → `webpack.prod.js`

### Modify HTML Template

Edit `src/template.html` - changes will be reflected automatically.

## 🤝 Contributing

Contributions are welcome! Here's how you can help:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 Best Practices

### Development Workflow

1. Work in the `src/` directory
2. Test changes using `npm run dev`
3. Build before deployment with `npm run build`
4. Deploy only the `dist/` folder

### Code Organization

- Keep modules in `src/modules/`
- Import dependencies at the top of files
- Use meaningful file and function names
- Document complex logic

### Performance

- Use code splitting for large applications
- Optimize images before adding to project
- Minimize external dependencies
- Test production builds regularly

### Security

- Avoid hardcoding sensitive information (e.g., API keys)
- Use HTTPS for secure communication

## 🐛 Troubleshooting

### Common Issues

**Webpack errors about module type:**

- Remove `"type"` property from `package.json`

**Dev server not updating:**

- Restart with `Ctrl+C` then `npm run dev`

**Images not loading:**

- Check file paths and webpack configuration
- Ensure images are in `src/` directory

**Build fails:**

- Clear `node_modules` and reinstall: `rm -rf node_modules && npm install`
- Check for syntax errors in webpack config files

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 👤 Author

**MatimotTheTimoters**

- GitHub: [@MatimotTheTimoters](https://github.com/MatimotTheTimoters)
- Repository: [top-submissions/template-webpack](https://github.com/top-submissions/template-webpack)

## 🙏 Acknowledgments

- [Webpack](https://webpack.js.org/) - Module bundler
- [date-fns](https://date-fns.org/) - Modern JavaScript date utility library
- [webpack-merge](https://github.com/survivejs/webpack-merge) - Configuration merging utility

## 📞 Support

If you encounter any issues or have questions:

- Check the [documentation](./docs/)
- Open an [issue](https://github.com/top-submissions/template-webpack/issues)
- Review the code comments in configuration files

## 🔄 Updates

This template is regularly updated to include:

- Latest Webpack features and best practices
- Security patches
- Performance improvements
- Community-requested features

Check the [commit history](https://github.com/top-submissions/template-webpack/commits) for recent changes.

---

**Made with ❤️ by MatimotTheTimoters | Template ready for production use**

## 🎯 Use Cases

This template is perfect for:

- Single-page applications (SPAs)
- Static websites with bundled assets
- Learning Webpack configuration
- JavaScript projects requiring module bundling
- Portfolio projects
- Prototype development
- Educational projects

Start building your next project with this template today! 🚀
