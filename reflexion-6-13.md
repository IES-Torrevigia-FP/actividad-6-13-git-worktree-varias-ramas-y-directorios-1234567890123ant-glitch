## Ventajas de git worktree

### Frente a cambiar de rama en el mismo directorio

Usar worktrees permite trabajar en varias ramas al mismo tiempo sin tener que cambiar constantemente de rama ni hacer stash de los cambios. Cada rama está en su propio directorio, lo que evita conflictos y pérdidas de tiempo al cambiar de contexto.

### Frente a clonar el repositorio varias veces

Los worktrees comparten el mismo repositorio interno (.git), por lo que ocupan menos espacio y son más rápidos de crear. En cambio, clonar varias veces duplica todo el historial y consume más recursos.

## Situaciones reales de uso

- Revisar una pull request mientras sigues desarrollando en otra rama sin interrumpir tu trabajo principal.
- Crear y probar un hotfix urgente sin afectar la rama en la que estás trabajando normalmente.

## Buenas prácticas

- Usar nombres claros para los directorios, por ejemplo con prefijo `wt-` (wt-feature-a, wt-bugfix, etc.).
- Mantener los worktrees organizados fuera del directorio principal del repositorio.
- Eliminar worktrees que ya no se utilizan para evitar desorden.
- Revisar periódicamente con `git worktree list` y limpiar con `git worktree prune` si es necesario.
