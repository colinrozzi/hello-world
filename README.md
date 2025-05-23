# Hello World Actor

A simple Theater actor for testing and demonstration purposes.

## Development

Build the actor locally:
```bash
cargo build --release --target wasm32-unknown-unknown
```

## Releasing

This actor uses automated releases via GitHub Actions.

### Creating a Release

1. Make your changes and commit them
2. Tag a new version:
   ```bash
   git tag v0.1.0
   git push origin v0.1.0
   ```
3. GitHub Actions will automatically:
   - Build the WASM component
   - Create a GitHub release
   - Upload the component and updated manifest

### Using a Released Actor

Reference the actor by its manifest URL:
```
https://github.com/OWNER/REPO/releases/download/v0.1.0/hello-world-manifest.toml
```

The manifest will contain URLs pointing to the release assets.

## Files Generated in Release

- `hello-world-component.wasm` - The WebAssembly component
- `hello-world-manifest.toml` - Manifest with GitHub release URLs
