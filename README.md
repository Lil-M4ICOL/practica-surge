# Práctica Surge – Despliegue continuo con GitHub Actions

Página HTML sencilla que se despliega automáticamente a
[surge.sh](https://lil-m4icol-practica-surge.surge.sh) con cada push a `main`.

## Estructura

```
.
├── index.html
├── README.md
└── .github/workflows/main.yaml
```

## Configuración

1. Instalar Surge: `npm install -g surge`
2. Crear la cuenta / iniciar sesión: `surge login`
3. Generar el token: `surge token`
4. En GitHub: **Settings → Secrets and variables → Actions → New repository secret** y crear:
   - `SURGE_LOGIN`: el correo de la cuenta de Surge
   - `SURGE_TOKEN`: el token generado con `surge token`
5. Hacer push a `main`; el workflow despliega la página.
