# Fix for JSX Runtime Error

## The Problem
The error `This JSX tag requires the module path 'react/jsx-runtime' to exist` occurs because TypeScript can't find the React type definitions.

## Solution

### Step 1: Install Dependencies
Open a terminal in your project directory and run:
```bash
npm install
```

This will install all required packages including `@types/react` and `@types/react-dom`.

### Step 2: Restart TypeScript Server
In VS Code/Cursor:
- Press `Ctrl+Shift+P` (or `Cmd+Shift+P` on Mac)
- Type "TypeScript: Restart TS Server"
- Press Enter

### Step 3: Verify
After restarting, the errors should disappear. The TypeScript configuration is already correct with:
- `"jsx": "react-jsx"` - Uses the new JSX transform
- `"moduleResolution": "bundler"` - Correct for Vite
- `"esModuleInterop": true` - Helps with module imports

## Why This Happens
The TypeScript language server needs access to the installed `@types/react` package in `node_modules` to understand JSX syntax. Without it, TypeScript can't find the `react/jsx-runtime` module.

