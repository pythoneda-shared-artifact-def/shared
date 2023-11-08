# shared-artifact

Artifact space for pythoneda-shared-artifact/shared

## How to declare it in your flake

Check the latest tag of the artifact repository: [https://github.com/pythoneda-shared-artifact/shared-artifact/tags](https://github.com/pythoneda-shared-artifact/shared-artifact/tags) and use it instead of the `[version]` placeholder below.

```nix
{
  description = "[..]";
  inputs = rec {
    [..]
    pythoneda-shared-artifact-shared = {
      [optional follows]
      url =
        "github:pythoneda-shared-artifact/shared-artifact/[version]?dir=shared";
    };
  };
  outputs = [..]
};
```

Should you use another PythonEDA modules, you might want to pin those also used by this project. The same applies to [nixpkgs](https://github.com/nixos/nixpkgs "nixpkgs") and [flake-utils](https://github.com/numtide/flake-utils "flake-utils").

Use the specific package depending on your system (one of `flake-utils.lib.defaultSystems`) and Python version:

- `#packages.[system].pythoneda-shared-artifact-shared-python38` 
- `#packages.[system].pythoneda-shared-artifact-shared-python39` 
- `#packages.[system].pythoneda-shared-artifact-shared-python310` 
- `#packages.[system].pythoneda-shared-artifact-shared-python311` 

The Nix flake is under the 
[infrastructure](https://github.com/pythoneda-shared-artifact/shared-artifact/tree/main/shared "shared") folder in <https://github.com/pythoneda-shared-artifact/shared-artifact>.
