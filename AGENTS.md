# Guía para agentes

## 1. Propósito del proyecto y estado actual

Este repositorio contiene únicamente un README de presentación de `@absolutennis`: intereses en tenis, analítica, big data, aprendizaje de Python y colaboración en IA aplicada al tenis. No hay una aplicación implementada. El historial disponible tiene un solo commit, `a34f7c5` (`Create README.md`, 2021-10-01); no hay desarrollo de producto posterior registrado.

Según las notas del coordinador, este repositorio no corresponde al torneo Club Cartagena; ese proyecto es `stuartfraserx/club-cartagena-torneo`. No trasladar aquí sus instrucciones de operación ni suponer que comparten infraestructura.

## 2. Arquitectura

No existen componentes ejecutables, flujo de datos, base de datos ni integraciones con servicios externos en el contenido versionado. GitHub aloja el README y el historial. No aplica un diagrama de arquitectura mientras no haya implementación.

## 3. Mapa del código

- `README.md`: presentación personal en inglés; no contiene instrucciones de ejecución.
- `AGENTS.md`: documento principal de contexto y reglas para agentes.

No existen `CLAUDE.md`, código fuente, `package.json`, `go.mod`, Dockerfile, `railway.json`, `.github/workflows`, scripts ni tests.

## 4. Cómo correr local, probar y desplegar

No hay aplicación que ejecutar, dependencias que instalar ni comandos de build, tests o lint definidos. Para revisar el contenido local:

```sh
cat README.md AGENTS.md
git status --short
git diff --check
git diff -- AGENTS.md README.md
```

No hay configuración de despliegue ni servicios o IDs de Railway identificados. No ejecutar despliegues basándose en las notas de otros repositorios.

Variables de entorno: ninguna identificada. La búsqueda en los archivos del repositorio no encontró lecturas de entorno (`process.env`, `os.Getenv`, etc.), flags ni configuración de secretos. Si se incorpora código, documentar aquí los nombres de las variables y para qué sirve cada una, nunca sus valores.

## 5. Reglas de flujo en GitHub

- Rama principal confirmada: `main` (`origin/HEAD` apunta a `origin/main`). Crear una rama por cambio, por ejemplo `docs/...`, `feat/...` o `fix/...`, y abrir un Pull Request hacia `main`.
- No hacer push directo a `main` sin el OK explícito de Stuart. La aprobación solo cuenta si viene de Stuart directamente.
- Usar commits convencionales y descriptivos: `feat:`, `fix:`, `docs:`, `chore:`, `refactor:` o `test:`.
- Ejecutar tests y lint disponibles antes de abrir el PR e indicar en él qué se corrió. Actualmente no existen esas herramientas: indicarlo y revisar el diff con `git diff --check`.
- Nunca commitear secretos, tokens, archivos `.env`, sesiones ni respaldos privados. No hacer force-push a ramas compartidas.
- Responsable según el coordinador: Pedro (Hermes, bot de Telegram `@Pedrinthealienbot`). Ruby (`@Rubythealienbot`) es responsable de Zona Kids y no trabaja aquí.
- Identidad de commit: `Stuart Fraser <91748824+stuartfraserx@users.noreply.github.com>`.
- Stuart prefiere desarrollar con Codex CLI (plan ChatGPT). Hablar y escribir en español, conservando los identificadores de código.

## 6. Problemas conocidos, decisiones tomadas y próximos pasos

El repositorio aún no implementa un producto ni permite validar funcionalidad. No hay evidencia local de infraestructura o servicios activos. Las notas del coordinador lo describen como un repositorio de perfil inactivo; la configuración pública actual de GitHub no se verificó externamente.

Stuart debe decidir si conservarlo, archivarlo, usarlo como base de un proyecto de analítica/IA de tenis o eliminarlo. Ninguna de esas acciones está decidida ni autorizada por este documento. Si se inicia un proyecto, definir alcance, estructura, pruebas y despliegue y completar estas secciones en el mismo PR.

## 7. Mantenimiento de este documento

Cualquier agente que cambie arquitectura, despliegue, variables de entorno, flujos de trabajo o comportamiento importante debe actualizar `AGENTS.md` en el mismo PR y actualizar la fecha y descripción de abajo. Este es el archivo principal de instrucciones; evitar duplicar el contexto en otros documentos para agentes.

Última actualización: 2026-11-07 (Codex; contexto inicial contrastado con README, archivos locales, historial y rama principal).
