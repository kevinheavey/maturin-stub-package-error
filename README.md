# maturin-stub-package-error
Example repo showing a bug in Maturin (I think)

This repo uses a directory of stub files to define type hints for a package instead of a single file. You can see [types-requests](https://github.com/python/typeshed/tree/master/stubs/requests/requests) for an example of this layout.

I haven't written the Rust code to make this example a package because it's irrelevant.

If you run `maturin develop` in this repo it fails with `Found a directory with the module name (solders) next to Cargo.toml, which indicates a mixed python/rust project, but the directory didn't contain an __init__.py file.`

