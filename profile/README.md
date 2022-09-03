# Script Manager
## Install
Download SCM with the following command:

`pastebin run 1kKZ8zTS`

## Naming Conventions
### Repositories
Libraries and Programs should each be created as an extra repository.

As an indicator libraries should have the suffix `-lib` and programs should have the suffix `-prog`.

The main script should always have the same name as the repository (without the suffix).

A repository should always have a `files.txt` in its root. The `files.txt` should contain all the paths to every file that should be downloaded by scm.

#### Example
Let's say we have a library called `test`.

The repository would be named `test-lib` and it would contain at least the following files:

- `test.lua`
- `files.txt`

`files.txt` would have at least the following line:

```
test.lua
```

### Requires
If you want to load a library within a program and keep it updated through SCM, then you can do that with the following notation:
```
--@requires testLibrary
require("testLibrary")
```
The comment tells SCM to look for the library and update it. If it's not already installed, then it will try to download it.
