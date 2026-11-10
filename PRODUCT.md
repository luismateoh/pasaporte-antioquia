# Product

<!-- impeccable:product-schema 1 -->

## Platform

web

## Users

- **Público general:** cualquier viajero que recibe el link (por redes o boca a boca) y quiere llevar la cuenta de los municipios de Antioquia que conoce.
- **Moteros y rodadas:** gente que recorre Antioquia en moto y usa el pasaporte para registrar los pueblos a los que llega.
- **Familia y amigos** del dueño, a quienes él les comparte el link.
- **El dueño (Luis)** usa el mismo pasaporte para su propio registro y es quien administra la lista de lugares.

La mayoría lo usa desde el celular, a menudo justo después de llegar a un pueblo o al repasar viajes pasados.

## Product Purpose

Un pasaporte de viajero de Antioquia: un sello ilustrado por cada uno de los 125 municipios (más algunos lugares extra) que la persona marca cuando lo visita. El objetivo principal es **animar a viajar**: que cada quien vea qué le falta, por subregión, y se motive a conocer el próximo pueblo. Éxito = que la gente vuelva a abrirlo para marcar un sello nuevo y planee viajes por los pendientes.

## Positioning

Cubre los 125 municipios reales de Antioquia, agrupados en sus 9 subregiones, cada uno con su propia ilustración de sello (paisaje, producto o lugar emblemático de ese municipio, nunca la iglesia/plaza genérica), y un mapa real del departamento que se pinta a medida que se visitan.

## Operating Context

- Se abre desde un link compartido; no hay instalación, cuentas ni registro.
- Marcar una visita es un solo toque sobre el sello; tocarlo otra vez lo desmarca. Sin fecha, nota ni otros campos.
- El progreso de cada persona vive solo en su navegador (`localStorage`); se puede mover entre dispositivos con Exportar/Importar (archivo JSON).
- Cada sello se puede ampliar, imprimir (hoja limpia de 10 cm) o descargar en PNG/SVG.

## Capabilities and Constraints

- Página estática de un solo archivo (`index.html`) publicada en GitHub Pages: https://luismateoh.github.io/pasaporte-antioquia/ (repo `luismateoh/pasaporte-antioquia`). Sin servidor ni cuentas; debe seguir así.
- La lista de lugares la administra solo el dueño en el código (municipios + `EXTRAS`). Los visitantes no pueden crear, borrar ni importar lugares; solo marcar o desmarcar visitas.
- Todo visitante nuevo arranca con el pasaporte vacío.
- El dueño irá agregando más lugares extra (sitios no municipales como Plaza Botero, Comuna 13, Cerro Tusa).
- La impresión de sellos físicos es una capacidad que debe mantenerse.
- Idioma: español de Colombia.

## Brand Commitments

- Nombre: «Pasaporte de viajero · Mis sellos de Antioquia».
- Sellos con ilustración propia por lugar, en estilo serigrafía vintage de cartel de viaje; las ilustraciones se generan con ChatGPT a partir de `assets/sellos/prompts.json` y se guardan como `assets/sellos/<id>.webp`.
- Bandera de Antioquia solo como banderita junto a «Pasaporte de viajero» (el dueño pidió quitar la bandera grande).

## Evidence on Hand

- 133 ilustraciones de sellos: `assets/sellos/*.webp` (125 municipios + 8 lugares extra), con sus prompts en `assets/sellos/prompts.json`.
- Paisaje del encabezado (casita paisa, café, montañas): `assets/paisaje.webp`.
- Límites reales de los 125 municipios embebidos en `index.html` (constante `MAPA`).
- No hay testimonios, cifras de uso ni prensa; no inventarlos.

## Product Principles

1. **Animar al próximo viaje:** lo pendiente debe verse tan claro como lo logrado.
2. **Un toque y listo:** registrar una visita no pide ningún dato.
3. **Cada pueblo con identidad propia:** el sello muestra lo que hace único al municipio.
4. **Sin fricción ni cuentas:** abrir el link basta; los datos son de cada quien.
5. **El catálogo lo cuida el dueño:** consistencia de la lista antes que contenido de usuarios.

## Accessibility & Inclusion

Uso principal en celular, en exteriores: objetivos táctiles de al menos 44 px y buen contraste. Respetar `prefers-reduced-motion`.
