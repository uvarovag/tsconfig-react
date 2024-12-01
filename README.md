# tsconfig-uvarovag

## for use in project

### 1. install dependencies

```bash
npm install --save-dev tsconfig-uvarovag typescript ts-node
```

### 2. create tsconfig.json

```json
{
    "extends": "tsconfig-uvarovag",
    // Файлы и папки, которые будут включены в процесс компиляции
    "include": [
        "src" // Только файлы в папке "src"
    ],
    // Файлы и папки, которые исключаются из процесса компиляции
    "exclude": [
        "node_modules", // Игнорирует папку "node_modules"
        "dist" // Игнорирует папку "dist" (собранный код)
    ],
    "compilerOptions": {
        // Указывает папку, куда будет компилироваться код
        "outDir": "./dist/",
        // Устанавливает базовый путь для всех относительных путей
        "baseUrl": "./",
        // Настраивает алиасы путей для удобного импорта модулей
        "paths": {
            "*": ["./src/*"] // Все импорты начинаются с "src"
        }
    }
}
```
