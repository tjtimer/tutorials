# Entwicklung einer Express.js-Webanwendung - Teil 1

1. Das Programm „curl“ installieren:
```bash
$ sudo apt-get install curl
```

2. Das Node.js-Paketarchiv hinzufügen: 
```bash
$ curl -sL https://deb.nodesource.com/setup_9.x | sudo -E bash –
```

3. Node.js installieren: 
```bash
$ sudo apt-get install -y nodejs 
```

4. Kontrollieren das Node.js funktioniert:
```bash
$ node -v
```

5. Einen Projektordner erstellen und hinein wechseln:
```bash
$ mkdir /var/www/my-app && cd /var/www/my-app
```

6. Starten eines Node.js-Projektes: 
```bash
$ npm init
```

7. Installation von Express.js:
```bash
$ npm i --save express
```

8. Datei „app.js“ erstellen und den nano-Editor öffnen:
```bash
$ nano app.js
```

9. Folgenden Javascript-Code einfügen und anschließend mit Strg-O speichern und mit Strg-X zum Terminal zurückkehren:
```javascript
const express = require("express");

const app = express();

app.get("/", function (request, response) {
	response.send("Hello World!");
});

app.listen(3000, function () {
	console.log("Your app is listening on port 3000!");
});
```

10. App starten:
```bash
$ node app.js
```

Fertig! Du kannst nun deine App unter http://localhost:3000/ im Browser deines Vertrauens aufrufen.