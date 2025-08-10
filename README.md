# ty-zed: `astral-sh/ty` for Zed

This extension provides [`ty`](https://github.com/astral-sh/ty), an extremely fast Python type checker and language server, for Zed editor.


> [!note]
> This extension has been officially merged into and is now maintained by the Zed team.
> 
> Please visit the new [repository](https://github.com/zed-extensions/ty) for the latest usage instructions and support.

## Installation
1.	Open Zed’s Extensions panel.
2.	Search for ty and install it.


## Enabling the Extension

Enable `ty` extension for Python in your Zed settings:

```jsonc
{
  "languages": {
    "Python": {
      "language_servers": ["ty"]
    }
  }
}
```

## Configuration

You must specify the binary path for ty under the lsp.ty.settings section.

### Example Setup

1.	Install `ty` (using [uv](https://github.com/astral-sh/uv) here as an example):

```bash
uv tool install ty
```

2.	Locate the binary:
```bash
which ty
```

3.	Configure Zed with the path and server arguments:

```jsonc
{
  "lsp": {
    "ty": {
      "binary": {
        "path": "/Users/yourname/.local/bin/ty",
        "arguments": ["server"]
      }
    }
  }
}
```

If `ty` is installed via another tool (e.g., pipx, system package manager), adjust the binary path accordingly.

