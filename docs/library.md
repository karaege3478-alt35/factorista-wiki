# OpenYerX's Library

Shared library for OpenYerX mods. Factorista requires it — without this mod installed alongside Factorista, the game will not start.

## For players

Just install it next to Factorista (and any OpenYerX addon). It has no GUI and does nothing visible on its own.

## For addon developers

Declare the `openyerx` entrypoint in your `fabric.mod.json`:

```json
"entrypoints": {
  "openyerx": ["com.example.MyAddon"]
}
```

Implement `com.openyerx.lib.api.OpenYerXPlugin`:

- `addonId()` returns your mod id.
- `onOpenYerXInit()` runs once at startup — register your content there.

The library discovers every registered plugin and logs them at boot.
