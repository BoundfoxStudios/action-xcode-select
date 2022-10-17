# xcode-select

This GitHub Action is a wrapper around `xcode-select` and will let you easily pick a specific Xcode version to be used in your workflow.

## Usage

The most basic usage will be without any inputs, which will default to `version: "latest"`

```yml
steps:
  - uses: BoundfoxStudios/xcode-select@v1
```

If you want to pin a specific version, specify it with the `version` input.

```yml
steps:
  - name: "Select the latest stable Xcode 12"
    uses: BoundfoxStudios/action-xcode-select@v1
    with:
      version: "12"
```

To test with an Xcode Beta release, use the `beta` input:

```yml
steps:
  - name: "Select the last available Xcode Beta"
    uses: BoundfoxStudios/xcode-select@v1
    with:
      beta: true
```

Although Apple does not use semantic versioning for Xcode, the GitHub virtual environments for macOS do, so you can use version numbers like `10.3.1` or `12.0.0`.

Look at the [actions/virtual-environments](https://github.com/actions/virtual-environments) project to find out which specific Xcode releases are included on the GitHub hosted runners.

## License

This action is released under the [MIT License](LICENSE).

## Contributions

Contributions are welcome. One of the most impactful things you can do is to file issues.

