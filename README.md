# SceneViewSwift — **archived mirror**

> ## ⚠️ This repository is a frozen mirror at `v4.0.0`.
> ### **For new projects, install from the [main SceneView monorepo](https://github.com/sceneview/sceneview) instead.**

```swift
// Package.swift
.package(url: "https://github.com/sceneview/sceneview.git", from: "4.3.4")
```

```
// Xcode: File → Add Package Dependencies…
https://github.com/sceneview/sceneview.git
```

The import is unchanged — `import SceneViewSwift`.

---

## What happened

This `sceneview/sceneview-swift` repository was created on **2026-04-12** as a Swift-Package-Manager mirror of the [`SceneViewSwift/`](https://github.com/sceneview/sceneview/tree/main/SceneViewSwift) subtree of the [main SceneView monorepo](https://github.com/sceneview/sceneview). Its first and only commit shipped the v4.0.0 source. The mirror was never re-synced: the monorepo went on to ship v4.0.1 through **v4.3.4+** while this mirror stayed frozen at v4.0.0.

In [sceneview#920](https://github.com/sceneview/sceneview/pull/920) the monorepo gained a root [`Package.swift`](https://github.com/sceneview/sceneview/blob/main/Package.swift), which made the mirror redundant — any SPM consumer can now point Xcode at the monorepo URL directly. [sceneview#1215](https://github.com/sceneview/sceneview/pull/1215) finished the retirement by migrating every doc / install snippet to the new URL.

---

## For existing consumers

If your `Package.resolved` is pinned to this mirror, your build keeps working — the `v4.0.0` tag is preserved and resolvable. But you'll be **4 minor versions behind** and won't receive bug-fixes or new features (the v4.3.4 lineup alone includes the AR Face Mesh exposure fix, ARCore Cloud Anchor recovery, Sketchfab UTF-8 decoding, plus the [#1215](https://github.com/sceneview/sceneview/pull/1215) skybox-renders fix that this mirror's [PR #1](https://github.com/sceneview/sceneview-swift/pull/1) seeded).

**To migrate** (Xcode):

1. Remove the dependency: select `sceneview-swift` in the project navigator → right-click → **Delete**.
2. Re-add: **File → Add Package Dependencies…** → enter `https://github.com/sceneview/sceneview.git` → choose **Up to Next Major** from `4.3.4`.
3. Re-add the `SceneViewSwift` library to your app target.

Source imports (`import SceneViewSwift`), public API, and the on-disk SDK code are identical between this mirror and the monorepo — only the SPM resolution URL changes.

---

## Contributors

If you'd like to contribute to SceneViewSwift, please open issues and pull requests on the monorepo: **<https://github.com/sceneview/sceneview>**.

Special thanks to **[@radcli14](https://github.com/radcli14)** (Eliott Radcliffe), who landed the first external PR on this mirror — [PR #1: Environment Skybox and Camera Orbit](https://github.com/sceneview/sceneview-swift/pull/1) — which was ported to the monorepo as [sceneview#1215](https://github.com/sceneview/sceneview/pull/1215) with co-authorship credit.

---

This repository is archived (read-only). The `v4.0.0` tag stays resolvable indefinitely for backwards compatibility; no further releases will be cut here.
