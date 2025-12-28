# Webpack Project Setup & Deployment Checklist

---

## 📋 Initial Project Setup

### 1. Create Project Directory and Initialize npm

- [x] Create new project directory

  ```bash
  mkdir your-project-name
  cd your-project-name
  ```

- [x] Initialize npm with default settings

  ```bash
  npm init -y
  ```

- [x] Open `package.json` and **remove** the `"type"` property if it exists (either `"commonjs"` or `"module"`)

---

## 📦 Install Core Dependencies

### 2. Install Webpack

- [x] Install webpack and webpack-cli as dev dependencies

  ```bash
  npm install --save-dev webpack webpack-cli
  ```

---

## 📁 Create Directory Structure

### 3. Set Up src and dist Directories

- [x] Create `src` directory for source code

  ```bash
  mkdir src
  ```

- [x] Create `src/index.js` file

### 4. Create .gitignore File

- [x] Create `.gitignore` in project root
- [x] Add the following content:

  ```
  node_modules
  dist
  ```

---

## ⚙️ Configure Webpack

### 5. Create webpack.config.js

- [x] Create `webpack.config.js` in project root
- [x] Add basic Webpack configuration

---

## 🌐 HTML Configuration

### 6. Install and Configure HtmlWebpackPlugin

- [x] Install html-webpack-plugin

  ```bash
  npm install --save-dev html-webpack-plugin
  ```

- [x] Create `src/template.html` file
- [ ] Add HTML skeleton to `template.html`
- [x] Update `webpack.config.js` to include HtmlWebpackPlugin

---

## 🎨 CSS Configuration

### 7. Install and Configure CSS Loaders

- [x] Install style-loader and css-loader

  ```bash
  npm install --save-dev style-loader css-loader
  ```

- [x] Create `src/styles.css` file
- [x] Update `webpack.config.js` to add CSS module rules
- [ ] Import CSS in `src/index.js`

---

## 🖼️ Image Configuration (If Needed)

### 8. Configure Image Handling

#### For Images in HTML Template

- [x] Install html-loader (if needed)
- [x] Add html-loader rule to webpack.config.js

#### For Images Used in JavaScript

- [x] Add asset/resource rule to webpack.config.js

---

## 🚀 Development Server Setup

### 9. Install and Configure webpack-dev-server

- [x] Install webpack-dev-server

  ```bash
  npm install --save-dev webpack-dev-server
  ```

- [x] Add devtool and devServer to `webpack.config.js`

---

## 📝 npm Scripts Configuration

### 10. Add npm Scripts to package.json

- [x] Update the `"scripts"` section in `package.json`

---

## ✅ Test Basic Setup

### 11. Verify Everything Works

- [ ] Add test content to `src/index.js`
- [ ] Run development build: `npm run build`
- [ ] Verify `dist` directory was created
- [ ] Start dev server: `npm run dev`

---

## 📤 Deployment to GitHub Pages

### 12. Initialize Git Repository

- [ ] Initialize git repository
- [ ] Add all files and make initial commit
- [ ] Create GitHub repository
- [ ] Link local repo to GitHub

### 13. Create gh-pages Branch

- [ ] Create gh-pages branch (one-time setup)

  ```bash
  git branch gh-pages
  ```

### 14. Deploy to GitHub Pages

**Follow these steps every time you deploy:**

- [ ] Ensure all changes are committed
- [ ] Switch to gh-pages and merge main

  ```bash
  git checkout gh-pages
  git merge main --no-edit
  ```

- [ ] Build the project

  ```bash
  npm run build
  ```

- [ ] Add dist folder to git

  ```bash
  git add dist -f
  git commit -m "Deployment commit"
  ```

- [ ] Push dist contents to gh-pages branch

  ```bash
  git subtree push --prefix dist origin gh-pages
  ```

- [ ] Switch back to main branch

  ```bash
  git checkout main
  ```

### 15. Enable GitHub Pages

- [ ] Go to GitHub repository → Settings → Pages
- [ ] Under "Source", select branch: `gh-pages`
- [ ] Select folder: `/ (root)`
- [ ] Click Save

---

## 📚 Additional Dependencies (Project-Specific)

### 16. Install Additional Libraries as Needed

- [x] Install date-fns (if project needs date manipulation)

  ```bash
  npm install date-fns
  ```

---

## 🔄 Updating Your Deployed Site

**Whenever you make changes and want to redeploy:**

1. [ ] Commit changes to main branch
2. [ ] Follow steps 14 (Deploy to GitHub Pages) again
3. [ ] Wait for GitHub Pages to update

---

**✅ Checklist Complete!** You now have a fully configured Webpack project ready for development and deployment!
