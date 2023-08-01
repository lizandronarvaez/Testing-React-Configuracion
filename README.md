# Pasos para configurar e instalar Jest + React Testing Library
## React + Vite

1. Instalaciones de dependencias:
    ```
    yarn add --dev jest babel-jest @babel/preset-env @babel/preset-react 
    yarn add --dev @testing-library/react @types/jest jest-environment-jsdom
    ```

2. Agregar un Script nuevo al package.json:
    ```
    "test": "jest --watchAll"
    ```

3. Crear archivo con el nombre de babel.config.json, con la siguiente configuracion:
    ```
    {
        "presets": [
            [
                "@babel/preset-env",
                {
                    "targets": {
                        "esmodules": true
                    }
                }
            ],
            [
                "@babel/preset-react",
                {
                    "runtime": "automatic"
                }
            ]
        ]
    }
    ```

4. Por ultimo crearemos un ultimo archivo  ```.babelrc``` :

    __.babelrc__
    ```
    {
        "presets": [
            "@babel/preset-env",
            "@babel/preset-react"
        ]
    }
    ```

## Con esto terminariamos la instalacion y configuracion
### Como ultimo paso tendriamos que ejectuar el script:

__Si utilizamos npm__
```
npm run test
```

__Si utilizamos yarn__
```
yarn test
```
