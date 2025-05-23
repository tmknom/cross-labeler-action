# cross-labeler-action

Run [actions/labeler][labeler] with configuration shared across repositories.

<!-- actdocs start -->

## Description

This action serves as a convenient wrapper for [actions/labeler][labeler].
Automatically assigning labels to new pull requests based on changed file paths or branch names, similar to [actions/labeler][labeler].

## Usage

To set up the action, you need to create a YAML file that defines your configurations.
Refer to the detailed configuration syntax for the labeler in [actions/labeler][labeler].

### Configuration URL

```yaml
  steps:
    - name: Cross Labeler
      uses: tmknom/cross-labeler-action@v0
      with:
        configuration-url: https://raw.githubusercontent.com/tmknom/configurations/main/labeler/conventional-commits.yml
```

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
| configuration-url | The url for the label configurations. | n/a | no |
| pr-number | The pull request number(s). | n/a | no |

## Outputs

| Name | Description |
| :--- | :---------- |
| configuration-path | The path for the configuration file to passing actions/labeler. |
| configuration-sha256 | SHA256 of the configuration file to passing actions/labeler. |

<!-- actdocs end -->

## Permissions

| Scope         | Access |
| :------------ | :----- |
| contents      | read   |
| pull-requests | write  |
| issues        | write  |

## FAQ

N/A

## Related projects

- [label-workflows](https://github.com/tmknom/label-workflows): Collection of label workflows.
- [configurations](https://github.com/tmknom/configurations): Collection of configurations.

## Release notes

See [GitHub Releases][releases].

[labeler]: https://github.com/actions/labeler
[conventional]: https://www.conventionalcommits.org
[releases]: https://github.com/tmknom/cross-labeler-action/releases
