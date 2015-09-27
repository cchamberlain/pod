# pod (WIP)
Cross-platform deployment toolkit with native dependencyless solutions for each platform.

### Installation
**`npm install -g pod-deploy`**

### Usage

**`pod [-d|-Diff path/to/left,path/to/right [-NoLeft|-NoRight]] [-g|-Generate] [-c|-PodfilePath path/to/podfile] [-p|-Porcelain] [path/to/pod]`**


### Podfile Format

```json
{ "targets":  [ { "name":     "SERVER_ONE"
               , "root":     "path/to/server/one/root"
               , "archive":  "path/to/archive/one/root"
               }
             , { "name":     "SERVER_TWO"
               , "root":     "/abs/path/to/server/root/two/root"
               , "archive":  "//unc-server/path/to/archive/two/root"
               }
             ]
}
```

**Defaults to looking in the root of the pod package for a podfile.json**

## Platforms
The goal of pod is to focus on installing a lightweight dependencyless deployment / web server solution with native implementations for each platform.

#### Windows
Windows implementation adds a pod.ps1 script into your `%SYSTEMROOT%\system32\PowerShell\v1.0` path which is automatically added into your PowerShell PATH environment variable. Supports PowerShell 3.0+ (Windows Server 2008+ Compatible)

To run from PowerShell, you must first set the execution policy on the machine.  In PowerShell, issue command `Set-ExecutionPolicy RemoteSigned`

#### Unix-like Systems
A bash implementation will be available soon that adheres to the same commands as pod in Windows.
