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
- rules: reglas para agentes de IA y lineamientos operativos del proyecto.
- rules incluye documentos como Agent.md y Colaboracion.md para ordenar el trabajo del equipo.
- view: vistas organizadas por rol de usuario.
- view/mesero: pantallas y flujos del rol mesero.
- view/cocinero: pantallas y flujos del rol cocinero.
- view/administrador: pantallas y flujos del rol administrador.

## Criterios de organizacion

- Lo reutilizable va en component; lo especifico de un rol va en view.
- Las reglas transversales del equipo o de agentes se centralizan en rules.
- Todo agente de IA debe leer los documentos .md de rules (por ejemplo, Agent.md) antes de modificar codigo.
- La asignacion de responsabilidades del equipo se define en rules/Colaboracion.md.
- Evitar duplicar utilidades: si algo se repite en mas de una vista, moverlo a utils, services o component segun corresponda.

## Como usar esta estructura

1. Define primero el rol afectado por la funcionalidad.
2. Si es una pantalla o flujo completo, crealo en view/mesero, view/cocinero o view/administrador.
3. Si el bloque se repetira en mas de una vista, ponlo en component.
4. Si necesitas logica de negocio o llamadas externas, colocalas en services.
5. Si necesitas funciones pequenas de apoyo, ponlas en utils.
6. Si hay configuraciones globales, variables o parametros, guardalos en config.
7. Si la funcionalidad requiere autenticacion o permisos, trabajala en auth.
8. Si necesitas datos de prueba o catalogos base, usalos desde data.
9. Si defines lineamientos operativos o reglas para agentes, documentalos en rules.
10. Antes de cualquier cambio de codigo realizado por agentes de IA, revisar y cumplir rules/Agent.md.
11. Antes de modificar carpetas compartidas, revisar la asignacion de responsables en rules/Colaboracion.md.

## Flujo sugerido para nuevas funcionalidades

1. Crea o ajusta la regla en rules si cambia el comportamiento esperado.
2. Implementa o adapta servicios en services.
3. Prepara datos de apoyo en data si hace falta.
4. Construye componentes reutilizables en component.
5. Integra la vista final en el rol correspondiente dentro de view.
6. Coloca recursos visuales en assets cuando aplique.

## Convencion simple de nombres

- component: nombres por tipo de bloque reutilizable.
- services: nombres por dominio de negocio.
- utils: nombres por accion corta y puntual.
- view: nombres por modulo de trabajo dentro de cada rol.


