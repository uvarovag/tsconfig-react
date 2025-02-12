# tsconfig-react

Shared TypeScript configuration for React projects using TypeScript.

## Installation

To use this configuration in your project, install the necessary dependencies:

```bash
npm install --save-dev @uvarovag/tsconfig-react typescript ts-node
```

## Usage

### Step 1: Create a `tsconfig.json` file

```json
{
    "extends": "@uvarovag/tsconfig-react",
    // Files and folders to be included in the compilation process
    "include": [
        "src" // Only files in the "src" folder
    ],
    // Files and folders to be excluded from the compilation process
    "exclude": [
        "node_modules", // Ignores the "node_modules" folder
        "dist" // Ignores the "dist" folder (compiled code)
    ],
    "compilerOptions": {
        // Sets the base path for all relative paths
        "baseUrl": "./",
        // Configures path aliases for convenient module imports
        "paths": {
            "*": ["./src/*"] // All imports start from "src"
        }
    }
}
```

### Step 2: Compile your project

```bash
npx tsc
```
