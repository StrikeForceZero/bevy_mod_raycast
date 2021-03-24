# Ray Casting for Bevy


[![CI](https://github.com/aevyrie/bevy_mod_raycast/workflows/CI/badge.svg?branch=master)](https://github.com/aevyrie/bevy_mod_picking/actions?query=workflow%3A%22CI%22+branch%3Amaster)
[![crates.io](https://img.shields.io/crates/v/bevy_mod_raycast)](https://crates.io/crates/bevy_mod_raycast)
[![docs.rs](https://docs.rs/bevy_mod_raycast/badge.svg)](https://docs.rs/bevy_mod_raycast)
[![Bevy tracking](https://img.shields.io/badge/Bevy%20tracking-main-lightblue)](https://github.com/bevyengine/bevy/blob/main/docs/plugins_guidelines.md#main-branch-tracking)

A [Bevy](https://github.com/bevyengine/bevy) plugin for ray casting. Used to build [`bevy_mod_picking`](https://github.com/aevyrie/bevy_mod_picking). Contributions welcome!

This plugin makes it simple to create ray casting sources, such as a transform (first person, third person shooter), or screenspace coordinates (mouse picking). Rays are shot from these sources every frame using a bevy system, and the intersections are stored in the ray casting source's component. 

- Only meshes that you mark with a component will be checked for intersections. 
- You can define which ray casting source(s) should interact with which mesh(es) by marking grouped sources and targets with the same type. 
- This plugin also provides some functionality to compute the intersection of rays with primitive shapes.
- Rudimentary acceleration is provided with opt-in bounding spheres.

## Bevy Version Support

I intend to track the `main` branch of Bevy. PRs supporting this are welcome! 

|bevy|bevy_mod_raycst|
|---|---|
|0.5|0.2|
|0.4|0.1|

## Demo

Run a rudimentary mouse picking example with:

```shell
cargo run --example mouse_picking --features="ex"
```