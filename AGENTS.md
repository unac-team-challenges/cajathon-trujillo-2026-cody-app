# AGENTS.md — cajathon-trujillo-2026-thetigers-app

Repo **público** del equipo TheTigers (Cajathon Trujillo 2026). Contiene la **interfaz web**: consume el contrato OpenAPI que publica `motor`.

Es parte de un metarepo. Si tienes acceso al repo padre privado `cajathon-trujillo-2026-thetigers`, su `AGENTS.md` y su `docs/INDICE.md` mandan sobre este archivo.

## Reglas

1. **Repo público:** nunca pegues aquí texto de las fichas de los desafíos, del Solution Concept ni de documentos del repo padre. Refiérete al desafío solo por su código.
2. Nunca hagas push a `main` ni a `develop`. Todo entra por PR contra `develop`.
3. Un agente nunca aprueba ni hace merge.
4. Solo datos sintéticos. Sin secretos: usa `.env` (ignorado) y documenta en `.env.example`.
5. Sin atribución de IA en el historial (`Co-Authored-By` de agentes, "Generated with…").
6. No agregues `LICENSE` sin acuerdo del equipo.

## Flujo

1. Issue en este repo, con criterio de aceptación.
2. Rama desde `develop`: `<tipo>/<issue>-<slug>`, por ejemplo `feat/12-grafo-de-relaciones`.
   ```bash
   gh issue develop 12 --base develop --name feat/12-grafo-de-relaciones --checkout
   ```
3. Commits en formato Conventional Commits. PR contra `develop` con un título `tipo(alcance): descripción` (lo valida la CI) y `Closes #12`.
4. 1 aprobación de otra persona y **Squash and merge**.
5. Release: PR `develop → main` titulado `release: vX.Y.Z`, con **merge commit** (nunca squash), y después tag.

## Verificaciones locales

```bash
# Pendiente de ADR-0003. Ejemplo para TypeScript: pnpm lint && pnpm test && pnpm build
```

## Estado

Stack pendiente de ADR-0003 en el repo padre. Al definirlo, actualiza la sección de verificaciones y el `.gitignore`.
