# pod
Cross-platform deployment tool with native dependencyless solutions for each platform.

## Windows
Windows implementation adds a pod.ps1 script into your path.

**usage: pod [-d|-Diff path/to/left,path/to/right [-NoLeft|-NoRight]] [-g|-Generate] [-c|-PodfilePath path/to/podfile] [-p|-Porcelain] [path/to/pod]**


## Podfile Format

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
