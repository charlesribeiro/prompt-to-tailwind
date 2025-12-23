# prompt-to-tailwind

A hands-on learning repository demonstrating Tailwind CSS development through progressive chapters for the book Prompt to Tailwind CSS, by Charles Ribeiro. Each chapter is organized as a separate Git branch, allowing you to explore different concepts and implementations step-by-step.

## Prerequisites

Before getting started, ensure you have the following installed:

- **Node.js** (v14 or higher) - [Download here](https://nodejs.org/)
- **npm** (comes with Node.js)
- **Live Server** or similar development server:
  - VS Code Extension: [Live Server by Ritwick Dey](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer)
  - Or any HTTP server of your choice (e.g., `python -m http.server`, `serve`, etc.)

## Setup Instructions

1. **Clone the repository:**
   ```bash
   git clone <repository-url>
   cd prompt-to-tailwind
   ```

2. **Install dependencies:**
   ```bash
   npm install
   ```

   This installs Tailwind CSS and other required packages defined in `package.json`.

3. **Choose a chapter to explore** (see navigation guide below)

## Navigating Between Chapters

Each chapter is stored as a separate Git branch. To switch between chapters and view different implementations:

### View Available Chapters
```bash
git branch -a
```

### Switch to a Specific Chapter
```bash
git checkout chapter-4   # Switch to Chapter 4
git checkout chapter-5   # Switch to Chapter 5
git checkout chapter-6   # Switch to Chapter 6
git checkout chapter-7   # Switch to Chapter 7
```

### Return to Main Branch
```bash
git checkout main
```

**Important:** After switching branches, you may need to run `npm install` again if dependencies differ between chapters.

## Running the Project

### Option 1: Using Live Server (Recommended for VS Code)

1. Open the project in VS Code
2. Switch to your desired chapter branch
3. Right-click on `index.html` (or the relevant HTML file)
4. Select "Open with Live Server"
5. Your browser will open automatically with live reload enabled

### Option 2: Using Other Development Servers

**Python 3:**
```bash
python -m http.server 8000
```

**Python 2:**
```bash
python -m SimpleHTTPServer 8000
```

**Node.js (http-server):**
```bash
npx http-server -p 8000
```

Then open your browser to `http://localhost:8000`

## Chapter Overview

- **Chapter 4**: Alpine.js integration and accessibility features
- **Chapter 5**: Advanced prompting techniques (persona-based, scaffolding, instructional)
- **Chapter 6**: Interactive components and Alpine.js calculator
- **Chapter 7**: Data visualization with charts and dashboards

## Development Workflow

1. Switch to a chapter branch
2. Run `npm install` (if first time on this branch)
3. Start your development server
4. Make changes to HTML/CSS files
5. Changes will be reflected automatically (with Live Server)

## Troubleshooting

**Styles not applying:**
- Ensure you've run `npm install` in the current branch
- Check that Tailwind CSS is properly configured in `tailwind.config.js`
- Verify the CSS file is being imported in your HTML

**Live Server not working:**
- Make sure the extension is installed and enabled
- Try refreshing the browser manually
- Check the browser console for errors

**Branch switching issues:**
- Commit or stash your changes before switching branches
- Use `git status` to check for uncommitted changes

## Contributing

When working on this repository:
- Each chapter should remain on its respective branch
- Follow the guidelines in `CLAUDE.md` for code standards
- Use mobile-first design principles with Tailwind CSS
