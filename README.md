# golang-basics

Some basic thing about Go development

## Init a ptoject

### 1. Local

```bash
cd $GOPATH
cd src
mkdir <projectname>
cd <projectname>
go mod init <projectname>
```

### 2. Remote

```bash
cd $GOPATH
cd src
mkdir <projectname>
cd <projectname>
```

## VS Code debug settings

Create the launch.json under the .vscode directory

`main.go` is the exact filename of the main module file

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

## Other info

1. Avoid to use port 5000 and 7000 on MacBook. They are used by MacOS

2. Install all required packages: `go get .`

3. Run go project: `go run .`
