# Morty Chat Widget

A standalone chat widget built with Angular Elements that can be used as a web component (`<morty-chat-widget>`) in any website or framework.

## Features

- 💬 Interactive chat interface
- 🔧 Standalone web component (no Angular required to use)
- 📦 Single JavaScript file bundle
- 🎨 Customizable styling
- 🚀 Easy integration with any website

## Quick Start

### Using the Widget

1. Include the JavaScript bundle in your HTML:
```html
<script src="path/to/morty-chat-widget.js"></script>
```

2. Use the web component in your HTML:
```html
<morty-chat-widget></morty-chat-widget>
```

### Complete Example

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>My Website</title>
</head>
<body>
  <h1>Welcome to My Website</h1>
  
  <!-- The chat widget -->
  <morty-chat-widget></morty-chat-widget>
  
  <!-- Load the widget script -->
  <script src="./morty-chat-widget.js"></script>
</body>
</html>
```

## Development

### Prerequisites

- Node.js (v18 or higher)
- npm

### Setup

1. Clone the repository
2. Install dependencies:
```bash
npm install
```

### Building the Widget

```bash
# Build the Angular widget and bundle it
npm run build:widget
```

This will:
1. Build the Angular widget (`npm run build`)
2. Bundle it into a single JS file (`npm run bundle`)
3. Output the final bundle to `demo/morty-chat-widget.js`

### Development Server

```bash
# Build and serve the demo
npm run dev
```

This will build the widget and start a local server at `http://localhost:8080` where you can test the widget.

### Individual Commands

```bash
# Build only the Angular widget
npm run build

# Bundle only (requires build first)
npm run bundle

# Serve the demo only
npm run serve:demo
```

## Project Structure

```
src/
├── widget.ts                 # Main entry point for the widget
└── app/
    └── chat-widget/
        ├── chat-widget.ts     # Chat widget component
        ├── chat-widget.html   # Component template
        └── chat-widget.scss   # Component styles

demo/
├── index.html                # Demo HTML page
└── morty-chat-widget.js      # Final bundled widget (generated)

dist/                         # Angular build output
rollup.config.js             # Rollup bundler configuration
angular.json                 # Angular CLI configuration
```

## How It Works

1. **Angular Elements**: The widget is built using Angular Elements, which allows Angular components to be used as custom elements (web components).

2. **Standalone Component**: The `ChatWidgetComponent` is a standalone Angular component that doesn't require an Angular module.

3. **Bundling**: Rollup bundles the Angular build output into a single JavaScript file that can be included in any HTML page.

4. **Web Component**: The final bundle registers the `<morty-chat-widget>` custom element that can be used anywhere.

## Customization

The widget can be customized by modifying the component files:

- **Functionality**: Edit `src/app/chat-widget/chat-widget.ts`
- **Styling**: Edit `src/app/chat-widget/chat-widget.scss`
- **Template**: Edit `src/app/chat-widget/chat-widget.html`

After making changes, run `npm run build:widget` to rebuild the bundle.

## Browser Support

The widget supports all modern browsers that support Custom Elements (Web Components):
- Chrome 67+
- Firefox 63+
- Safari 10.1+
- Edge 79+

## License

UNLICENSED - Internal use only
