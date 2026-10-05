# NixieFX and Babylon Node Particle Editor: two workflows

This repository accompanies an original comparison of two independent browser particle effects. The NixieFX effect runs in PixiJS 8; the Babylon Node Particle Editor example runs in a Babylon.js scene. They do not share an effect format, and this is not a performance benchmark or a parity test.

![Observed NixieFX burst beside Babylon NPE effect](nixiefx-vs-babylon-npe.png)

## Reproduce

1. Download [the source archive](n014-source.zip) and extract it.
2. In the extracted directory, run `npm ci`.
3. Run `./node_modules/.bin/nixie-fx validate ./vfx-project`.
4. Run `npm run dev` and open the local address printed by Vite.
5. Press **Replay NixieFX burst** and **Save observed screenshot**.

The page fetches the pinned `babylonjs@9.27.1` UMD bundle from jsDelivr and Babylon's public Node Particle Editor snippet `#8O4BJ2`. These services must be reachable. The NixieFX exported effect and source project are bundled in the archive. The preview reports loading errors instead of presenting a blank comparison silently.

Validation on October 5, 2026 reported zero errors, zero warnings and two informational notes about PixiJS depth semantics. The Vite production build completed. Both effects rendered in a local browser, and the screenshot above was captured from that page. No frame time, memory, visual parity or device performance measurements were taken.

Source and method are described in `ARTICLE.md` inside the archive. Babylon's NPE example: https://forum.babylonjs.com/t/new-feature-the-node-particle-editor-npe/59303. NixieFX runtime documentation: https://nixiefx.com/vfx-runtime-docs/.
