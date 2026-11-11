---
title: "Lección 12 - Publica el sitio con GitHub Pages"
description: "Usa la aplicación GitHub Copilot para configurar un flujo de trabajo de Pages, revisar su pull request y verificar que Space Quiz está disponible."
authors:
  - jamesmontemagno
lastUpdated: 2026-10-12
---

Publica Space Quiz con GitHub Pages para que todo el mundo pueda acceder a ella. Copilot puede preparar el flujo de trabajo y guiarte durante la implementación, pero tú eres responsable de revisar los cambios y confirmar que el sitio está disponible.

En esta lección:

- pedirás a Copilot que configure una implementación con GitHub Pages.
- revisarás el flujo de trabajo y el pull request antes de fusionarlo.
- seguirás la implementación y comprobarás el sitio publicado.

## Escenario

Space Quiz ya está en un repositorio de GitHub, pero hace falta una forma sencilla de probarla. Publicar el sitio de un solo archivo con GitHub Pages permite acceder a él mediante una URL pública sin añadir un servidor ni una dependencia de runtime.

## Pide a Copilot que publique el sitio

En la sesión de la aplicación Copilot para `space-quiz`, envía este prompt:

```plaintext
Habilita GitHub Pages para este repositorio. Crea un flujo de trabajo de GitHub Actions que compile el sitio web si es necesario y lo implemente en GitHub Pages. Añade un README que describa la aplicación y cómo ejecutarla localmente si aún no existe. Crea un pull request con estos cambios y fusiónalo cuando se superen las comprobaciones obligatorias. Supervisa la implementación hasta que finalice correctamente y, después, indica la URL final del sitio web publicado. Si no tienes permiso para habilitar Pages o fusionar, dime exactamente qué debo aprobar o hacer; no informes de que se ha completado hasta que el sitio esté disponible.
```

![Diagrama en tres etapas: un pull request de space-quiz fusionado; una ejecución correcta de GitHub Actions Deploy website con los pasos Build website, Upload artifact y Deploy to Pages; y Space Quiz publicado en yourname.github.io/space-quiz/.](../../../_images/first-steps-app-pages-deploy.svg)

> [!WARNING]
> Este prompt pide al agente que cree y fusione un pull request y cambie la configuración de Pages del repositorio. Revisa las diferencias, los permisos de implementación y cualquier solicitud de aprobación de GitHub antes de continuar.

## Revisa el flujo de trabajo y verifica la implementación

1. Confirma que el README solo se ha añadido si el repositorio aún no tenía uno.
2. Revisa los cambios del pull request, incluidos los pasos de compilación e implementación del flujo de trabajo.
3. Fusiona los cambios solo después de que se superen las comprobaciones obligatorias del pull request.
4. Sigue la ejecución de implementación de GitHub Actions hasta que finalice correctamente.
5. Abre la URL indicada y confirma que Space Quiz se carga.

Si el agente no puede habilitar Pages ni fusionar el pull request, sigue las instrucciones específicas que te proporcione. No des la tarea por terminada hasta que la implementación se complete y el sitio esté disponible.

## Resumen y próximos pasos

Space Quiz ya está publicado y has verificado la implementación en lugar de confiar únicamente en el informe del agente. Continúa con la [lección 13: Repaso y próximos pasos][next-lesson].

[next-lesson]: ../13-review/
