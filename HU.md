# Go fejleszési alapok

## Projekt létrehozás


```bash
mkdir <projectname>
cd <projectname>
go mod init <projectname>
```


## Visual Studio Code debug beállítások

1. Hozdd létre a `launch.json` fájlt a `.vscode` mappában
2. `main.go` az projekt fő állománya. Ehhez állítjuk be a hibakeresést is

```json
{
  // Use IntelliSense to learn about possible attributes.
  // Hover to view descriptions of existing attributes.
  // For more information, visit: https://go.microsoft.com/fwlink/?linkid=830387
  "version": "0.2.0",
  "configurations": [
    {
      "name": "Launch file",
      "type": "go",
      "trace": "verbose",
      "showLog": true,
      "logOutput": "dap",
      "request": "launch",
      "mode": "debug",
      "program": "${workspaceFolder}/main.go"
    }
  ]
}
```

##Egyéb

1. MacOS esetén kerüld a projektekben az 5000-es és a 7000-es portok használatát, mert ezek használatban vannak az OS által.
2. Szükséges csomagok telepítése: `go get .`
3. Projekt futtatása: `go run .` vagy `go run main.go`
