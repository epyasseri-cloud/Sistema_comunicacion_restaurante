# Estructura base del proyecto restaurante

Este proyecto inicia con una estructura de carpetas pensada para separar responsabilidades por dominio y por rol operativo.

## Arbol de carpetas

```text
Proyecto integrador restaurante/
|- assets/
|- auth/
|- component/
|- config/
|- services/
|- data/
|- utils/
|- rules/
|- view/
|  |- mesero/
|  |- cocinero/
|  |- administrador/
|- README.md
```

## Descripcion de cada carpeta

- assets: recursos estaticos como imagenes, iconos, tipografias y archivos multimedia.
- auth: flujo de autenticacion y autorizacion.
- component: componentes reutilizables de interfaz o bloques compartidos.
- config: configuraciones globales, constantes y parametros del proyecto.
- services: logica de servicios, integraciones y comunicacion con APIs o backend.
- data: datos base, mocks, catálogos o estructuras de apoyo.
- utils: funciones auxiliares y utilidades reutilizables.
- rules: reglas para agentes y lineamientos operativos o de negocio.
- view: vistas organizadas por rol de usuario.
- view/mesero: pantallas y flujos del rol mesero.
- view/cocinero: pantallas y flujos del rol cocinero.
- view/administrador: pantallas y flujos del rol administrador.

## Criterios de organizacion

- Lo reutilizable va en component; lo especifico de un rol va en view.
- Las reglas transversales del equipo o de agentes se centralizan en rules.
- Evitar duplicar utilidades: si algo se repite en mas de una vista, moverlo a utils, services o component segun corresponda.


