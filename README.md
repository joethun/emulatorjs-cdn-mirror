<div align="center">
  <img width="300" src="https://cdn.jsdelivr.net/gh/EmulatorJS/EmulatorJS@main/docs/Logo-light.png">
  <h3>EmulatorJS CDN Mirror</h3>
  <p>A daily mirror of the EmulatorJS stable and nightly CDNs, served via jsDelivr.</p>

  ![Mirror - Stable](https://github.com/joethun/emulatorjs-cdn-mirror/actions/workflows/mirror-stable.yml/badge.svg)
  ![Mirror - Nightly](https://github.com/joethun/emulatorjs-cdn-mirror/actions/workflows/mirror-nightly.yml/badge.svg)
  [![EmulatorJS](https://img.shields.io/badge/EmulatorJS-GitHub-181717?logo=github)](https://github.com/EmulatorJS/EmulatorJS)
</div>

---

## Usage

Set `EJS_pathtodata` in your EmulatorJS config to one of the URLs below:

| Build | URL |
|-------|-----|
| Stable | `https://cdn.jsdelivr.net/gh/joethun/emulatorjs-cdn-mirror@main/stable/` |
| Nightly | `https://cdn.jsdelivr.net/gh/joethun/emulatorjs-cdn-mirror@main/nightly/` |

Stable is recommended as nightly could be unstable.

## Example

```html
<script>
  fetch("https://cdn.jsdelivr.net/gh/joethun/emulatorjs-cdn-mirror@main/EmulatorJS.html")
    .then(res => res.text())
    .then(html => {
      document.open();
      document.write(html);
      document.close();
    });
</script>
```