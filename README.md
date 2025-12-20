<div align="center">
  <img src="https://cdn.jsdelivr.net/gh/EmulatorJS/EmulatorJS@main/docs/Logo-light.png" width="275"/><br>
  
  #
  
  **https://github.com/EmulatorJS/EmulatorJS**
  
</div>

> [!NOTE]  
> **This project was not created by me. See link above.**

<div align="center">
  
  ## Example HTML:
</div>

<div align="center">
    This allows you to use it on hosting platforms with ease, such as Google Sites.
</div><br>


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
