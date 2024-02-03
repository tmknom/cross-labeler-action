# cross-labeler-action

A convenient wrapper for [actions/labeler][labeler].

<!-- actdocs start -->

## Description

This action serves as a convenient wrapper for [actions/labeler][labeler].
Automatically assigning labels to new pull requests based on changed file paths or branch names, similar to [actions/labeler][labeler].

## Usage

To set up the action, you need to create a YAML file that defines your configurations.
Refer to the detailed configuration syntax for the labeler in [actions/labeler][labeler].

### Configuration Path

```yaml
  steps:
    - name: Cross Labeler
      uses: tmknom/cross-labeler-action@v0
      with:
        configuration-path: .github/labeler.yml
```

## Inputs

| Name | Description | Default | Required |
| :--- | :---------- | :------ | :------: |
| configuration-path | The path for the label configurations. | n/a | no |

## Outputs

N/A

<!-- actdocs end -->

## Permissions

| Scope         | Access |
| :------------ | :----- |
| contents      | read   |
| pull-requests | write  |

## FAQ

N/A

## Release notes

See [GitHub Releases][releases].

## License

Apache 2 Licensed. See [LICENSE](LICENSE) for full details.

[labeler]: https://github.com/actions/labeler
[releases]: https://github.com/tmknom/cross-labeler-action/releases
