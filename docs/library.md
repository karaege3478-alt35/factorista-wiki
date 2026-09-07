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

## Creative tabs

```java
CreativeTabs.addItemToCreativeTab(MY_ITEM, CreativeTabs.Tab.FACTORISTA);
```

One call puts your item into any of the 10 vanilla main tabs
(Building Blocks, Decorations, Redstone, Transportation, Food and Drink,
Tools, Combat, Brewing, Ingredients, Spawn Eggs) or Factorista's own tab.
No event code needed.

Custom tabs from other mods work too:

```java
CreativeTabs.addItemToCreativeTab(PURPLE_DIAMOND, "hujujuju", "main");
```

## One-line items

```java
public static final Item MY_GEM = LibItems.addItem("mymod", "my_gem", CreativeTabs.Tab.INGREDIENTS);
```

Registers the item and tabs it in one call (call during mod init).
Model, texture and name still come from your assets.
