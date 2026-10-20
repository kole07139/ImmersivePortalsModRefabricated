# Changelog

## 0.1.0 — Minecraft 1.21.4

- Establish the Immersive Portal Refabricated identity, Maven group and repository links while retaining upstream attribution, save namespaces and Java API packages.
- Port the 1.21.1 implementation, including the bundled DimLib, to the Minecraft 1.21.4 registries, entity factories, movement packets, interaction results and rendering APIs.
- Pin Java 21, Gradle 8.11.1, Loom 1.9.2, Fabric API 0.119.4, Sodium 0.6.13 and Iris 1.8.8.
- Fix the world creation screen constructor injection that crashed before entering a world.
- Update chunk render section indices, camera section tracking and occlusion graph invalidation to restore terrain rendering.
- Bind and restore the projection used by portal screen triangles and register core shaders through the public preload list.
- Remap the RenderSystem shader Mixin descriptors correctly in distributed JARs.
- Initialize the fog context before the first ordinary client world frame.
- Encode player position dimensions on dedicated servers and decode them conditionally on modded clients.
- Supply 1.21.4 item model definitions for the portal helper, portal wand and command stick.
- Include a versioned compatibility identity for the historical `immersive_portals` API so the new fork version works with Iris.
- Bind clipping uniforms to the correct OpenGL program and discover uniforms lazily for Iris shader subclasses.
- Use the 1.21.4 blit sampler name to restore visible portal and GUI framebuffer images with shader packs.
- Cancel pending GUI renders after their target is disposed, restore the main framebuffer on exceptions and update Iris depth attachments when switching equally-versioned targets.
- Remove stale portal collision references when a destination dimension disappears and filter DimLib registry holes when saving world dimensions.
- Wait for the requested chunk ticking state without treating the unloaded sentinel as a failed load.
- Redirect the new server-side pick-block request through portals while retaining vanilla inventory/NBT checks and Fabric callbacks.
- Package upstream licenses, fork-specific terms and modification notices in reproducible binary and source archives.
- Add separate, remapped in-game regression tests and clean client/server launch tools. Detailed outcomes and any outstanding validation are recorded in [the porting report](docs/PORTING-1.21.4.md).

Historical changes remain available in the Git history and original branches.
