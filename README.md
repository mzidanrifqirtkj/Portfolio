<div align="center">
  <img alt="Logo" src="https://raw.githubusercontent.com/bchiang7/v4/main/src/images/logo.png" width="100" />
</div>
<h1 align="center">
  Personal Portfolio Website - v4
</h1>
<p align="center">
  A modern personal portfolio website built with <a href="https://www.gatsbyjs.org/" target="_blank">Gatsby 5</a>, <a href="https://reactjs.org/" target="_blank">React 18</a>, and <a href="https://styled-components.com/" target="_blank">Styled Components</a>
</p>
<p align="center">
  <strong>✨ Updated to latest technologies for Node.js v20+ compatibility</strong>
</p>

<p align="center">
  <a href="https://github.com/mzidanrifqirtkj/Portfolio/actions/workflows/ci.yml">
    <img src="https://github.com/mzidanrifqirtkj/Portfolio/actions/workflows/ci.yml/badge.svg" alt="CI Status" />
  </a>
  <a href="https://github.com/mzidanrifqirtkj/Portfolio/actions/workflows/deploy-vercel.yml">
    <img src="https://github.com/mzidanrifqirtkj/Portfolio/actions/workflows/deploy-vercel.yml/badge.svg" alt="Vercel Deployment" />
  </a>
</p>

![demo](https://raw.githubusercontent.com/bchiang7/v4/main/src/images/demo.png)

## � Tech Stack

This portfolio leverages modern web technologies:

- **Frontend Framework**: [Gatsby 5.15.0](https://www.gatsbyjs.org/) - Static site generator with React
- **UI Library**: [React 18.2.0](https://reactjs.org/) - Component-based UI library
- **Styling**: [Styled Components 6.1.8](https://styled-components.com/) - CSS-in-JS styling
- **Data Layer**: [GraphQL 16.8.1](https://graphql.org/) - Query language for APIs
- **Image Processing**: [Gatsby Plugin Image](https://www.gatsbyjs.com/plugins/gatsby-plugin-image/) - Optimized image loading
- **Content Management**: Markdown files with frontmatter
- **Analytics**: Google Analytics 4 via gatsby-plugin-google-gtag
- **Node.js**: v18+ (tested with v20.19.3)

## �🚨 Forking this repo (please read!)

Many people have contacted me asking me if they can use this code for their own website, and the answer to that question is usually **yes, with attribution**.

I value keeping my site open source, but as you all know, _**plagiarism is bad**_. It's always disheartening whenever I find that someone has copied my site without giving me credit. I spent a non-trivial amount of effort building and designing this iteration of my website, and I am proud of it! All I ask of you all is to not claim this effort as your own.

Please also note that I did not build this site with the intention of it being a starter theme, so if you have questions about implementation, please refer to the [Gatsby docs](https://www.gatsbyjs.org/docs/).

### TL;DR

Yes, you can fork this repo. Please give me proper credit by linking back to [brittanychiang.com](https://brittanychiang.com). Thanks!

## 🛠 Installation & Set Up

### Prerequisites

- **Node.js**: v18.0.0 or higher
- **npm**: v8.0.0 or higher
- **Git**: For version control

### Quick Start

1. **Clone the repository**

   ```sh
   git clone https://github.com/yourusername/portfolio.git
   cd portfolio
   ```

2. **Install the Gatsby CLI** (if you haven't already)

   ```sh
   npm install -g gatsby-cli
   ```

3. **Install dependencies**

   ```sh
   npm install
   ```

4. **Start the development server**

   ```sh
   npm start
   ```

5. **Open your browser** and visit `http://localhost:8000`

### Alternative: Using Yarn

```sh
yarn install
yarn start
```

## 📜 Available Scripts

| Command          | Description                          |
| ---------------- | ------------------------------------ |
| `npm start`      | Start the development server         |
| `npm run build`  | Build the site for production        |
| `npm run serve`  | Preview the production build locally |
| `npm run clean`  | Clear Gatsby cache and public folder |
| `npm run format` | Format code with Prettier            |

## 🚀 Building and Running for Production

1. **Generate a full static production build**

   ```sh
   npm run build
   ```

2. **Preview the site as it will appear once deployed**

   ```sh
   npm run serve
   ```

3. **Deploy to Netlify**
   - Connect your GitHub repository to Netlify
   - Set build command: `npm run build`
   - Set publish directory: `public`

## 📁 Project Structure

```
├── content/                 # Markdown content
│   ├── featured/           # Featured projects
│   ├── jobs/               # Work experience
│   ├── posts/              # Blog posts
│   └── projects/           # Other projects
├── src/
│   ├── components/         # React components
│   ├── hooks/              # Custom React hooks
│   ├── images/             # Image assets
│   ├── pages/              # Gatsby pages
│   ├── styles/             # Global styles and theme
│   ├── templates/          # Page templates
│   └── utils/              # Utility functions
├── static/                 # Static assets
├── gatsby-config.js        # Gatsby configuration
├── gatsby-node.js          # Gatsby Node APIs
└── package.json           # Dependencies and scripts
```

## ⚙️ Configuration

### Site Metadata

Edit `gatsby-config.js` to update site information:

```javascript
siteMetadata: {
  title: 'Your Name',
  description: 'Your description',
  siteUrl: 'https://yourwebsite.com',
  // ...
}
```

### Personal Information

Update `src/config.js` with your personal details:

```javascript
module.exports = {
  email: 'your.email@gmail.com',
  socialMedia: [
    // Your social media links
  ],
  navLinks: [
    // Navigation links
  ],
  // ...
};
```

## 🎨 Customization

### Colors and Theme

- Edit `src/styles/theme.js` to customize colors, fonts, and design tokens
- Dark mode is supported by default with automatic system preference detection

### Content Management

- **About Section**: Edit `src/components/sections/about.js`
- **Work Experience**: Add/edit markdown files in `content/jobs/`
- **Featured Projects**: Add/edit markdown files in `content/featured/`
- **All Projects**: Add/edit markdown files in `content/projects/`
- **Blog Posts**: Add/edit markdown files in `content/posts/`

### Images and Assets

- **Profile Picture**: Replace `src/images/me.jpg`
- **Favicon**: Replace files in `src/images/favicons/`
- **Resume**: Replace `static/resume.pdf`

## 🚀 CI/CD and Deployment

This project includes automated CI/CD workflows powered by GitHub Actions and deployment to Vercel.

### GitHub Actions Workflows

#### 1. **CI Workflow** (`.github/workflows/ci.yml`)
Runs on every push and pull request to `main` and `develop` branches.

- **Tests on**: Node.js 18.x and 20.x
- **Checks**:
  - ESLint code linting
  - Prettier code formatting
  - Gatsby production build
- **Artifacts**: Uploads build artifacts for Node 18.x

#### 2. **Vercel Deployment** (`.github/workflows/deploy-vercel.yml`)
Automatically deploys to Vercel.

- **Production**: Deploys to production on push to `main` branch
- **Preview**: Creates preview deployments for pull requests
- **Manual**: Can be triggered manually via workflow dispatch

#### 3. **Dependency Check** (`.github/workflows/dependency-check.yml`)
Weekly security audit of dependencies.

- **Schedule**: Runs every Sunday at midnight UTC
- **Checks**:
  - npm security audit (moderate level)
  - Outdated packages check

#### 4. **Code Quality** (`.github/workflows/code-quality.yml`)
Runs on pull requests to ensure code quality.

- **Checks**: Runs lint-staged for staged files

### Setting Up Vercel Deployment

To enable automatic deployments to Vercel, you need to configure the following secrets in your GitHub repository settings:

1. Go to your repository **Settings → Secrets and variables → Actions**
2. Add the following secrets:

| Secret Name | Description | How to Get |
|-------------|-------------|------------|
| `VERCEL_TOKEN` | Personal Access Token from Vercel | Create at [Vercel Account Settings → Tokens](https://vercel.com/account/tokens) |
| `VERCEL_ORG_ID` | Your Vercel Organization ID | Run `vercel link` in your project and find in `.vercel/project.json` |
| `VERCEL_PROJECT_ID` | Your Vercel Project ID | Run `vercel link` in your project and find in `.vercel/project.json` |

#### Getting Your Vercel IDs

```sh
# Install Vercel CLI
npm install -g vercel

# Link your project to Vercel
vercel link

# Your IDs will be saved in .vercel/project.json
cat .vercel/project.json
```

**Note**: The `.vercel` directory is gitignored, so your IDs won't be committed to the repository.

### Manual Deployment to Vercel

You can also deploy manually using the Vercel CLI:

```sh
# Install Vercel CLI globally
npm install -g vercel

# Deploy to preview
vercel

# Deploy to production
vercel --prod
```

## 🤝 Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- Original design inspiration and code structure
- Gatsby.js community and documentation
- React and styled-components communities
