# Asignacion de deberes y control de cambios

Este documento define una asignacion base de responsabilidades para evitar conflictos de cambios en el codigo dentro del proyecto.

## Objetivo

Separar el trabajo por zonas del proyecto y establecer una regla clara para carpetas compartidas.

## Asignacion recomendada por areas

### DIANA

Responsable principal de:
- view/mesero
- view/cocinero
- assets relacionados con mesero y cocinero
- data usada por mesero y cocinero

### YASSER

Responsable principal de:
- view/administrador
- auth
- assets relacionados con administrador
- data compartida
- component
- services
- utils
- config
- rules

## Regla para carpetas compartidas

Las carpetas component, services, utils, config, rules y cualquier data compartida no deben ser modificadas al mismo tiempo por varias personas sin coordinacion previa.

## Politica de trabajo

1. Cada integrante trabaja primero en su carpeta asignada.
2. Si necesita tocar una carpeta compartida, debe avisar al responsable principal antes de hacer cambios.
3. Si dos personas necesitan editar el mismo archivo, una hace el cambio y la otra espera revision o trabaja sobre una rama separada.
4. Ningun cambio en carpetas compartidas debe llegar a la rama principal sin revision.
5. Toda nueva funcionalidad debe intentar dejar la logica comun en component, services o utils, no duplicada en varias views.

## Regla de ramas recomendada

1. main queda solo para versiones estables.
2. Cada integrante usa su propia rama de trabajo.
3. Nombre sugerido de ramas:
   - feature/integrante1-nombre
   - feature/integrante2-nombre
4. Los cambios se integran a main solo despues de revisar conflictos.

## Regla para agentes de IA

1. Antes de modificar codigo, el agente debe leer Agent.md y este documento.
2. Si el cambio afecta una carpeta compartida, el agente debe indicarlo en su respuesta.
3. Si el cambio cruza mas de un area de responsabilidad, el agente debe advertir que puede generar conflictos de integracion.

## Procedimiento rapido antes de editar

1. Confirmar que carpeta se va a modificar.
2. Confirmar quien es el responsable principal de esa carpeta.
3. Confirmar si la carpeta es compartida o exclusiva.
4. Hacer cambios pequenos y acotados.
5. Revisar conflictos antes de integrar.
