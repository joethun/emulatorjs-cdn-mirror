<div align="center">
  <img src="https://cdn.jsdelivr.net/gh/EmulatorJS/EmulatorJS@main/docs/Logo-light.png" width="275"/>
  <br><br>
  <strong><a href="https://github.com/EmulatorJS/EmulatorJS">https://github.com/EmulatorJS/EmulatorJS</a></strong>
</div>

> [!NOTE]
> This project was not created by me. See the link above for the original project.

## Configuration

Depending on which version you would like to use, set your EJS_pathtodata to one of the following:

- **Nightly**: `https://cdn.jsdelivr.net/gh/joethun/emulatorjs-cdn-mirror@main/nightly/`
- **Stable**: `https://cdn.jsdelivr.net/gh/joethun/emulatorjs-cdn-mirror@main/stable/`

## Usage (Google Sites / Hosting)

This simple HTML allows you to use it on hosting platforms with ease, such as Google Sites.

```html
<!doctype html>
<html>
<body>
    <script>
        ejs();
        function ejs() {
            try {
                fetch("https://cdn.jsdelivr.net/gh/joethun/emulatorjs-cdn-mirror@main/EmulatorJS.html?t=" + Date.now())
                    .then(response => response.text())
                    .then(html => {
                        document.documentElement.innerHTML = html;
                        document.documentElement.querySelectorAll('script').forEach(oldScript => {
                            const newScript = document.createElement('script');
                            if (oldScript.src) {
                                newScript.src = oldScript.src;
                            } else {
                                newScript.textContent = oldScript.textContent;
                            }
                            document.body.appendChild(newScript);
                        });
                    });
            } catch (error) {
                console.error('error:', error);
            }
        }
    </script>
</body>
</html>
```
