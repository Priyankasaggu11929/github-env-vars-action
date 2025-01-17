# :octocat: :rocket: GitHub Environment Variables Action

A [GitHub Action](https://github.com/features/actions) to expose useful environment variables.

### Environment Variables exposed by **this Action**

| Environment Variable Name | Description                                                                                                                           | Example value             |
|---------------------------|---------------------------------------------------------------------------------------------------------------------------------------|---------------------------|
| `GITHUB_REPOSITORY_OWNER` | The owner of the repository.                                                                                                          | `FranzDiebold`            |
| `GITHUB_REPOSITORY_NAME`  | The name of the repository.                                                                                                           | `github-env-vars-action`  |
| `GITHUB_REF_NAME`         | The branch name that triggered the workflow. If neither a branch or tag is available for the event type, the variable will not exist. | `feature-branch-1`        |
| `GITHUB_SHA_SHORT`        | The shortened commit SHA (8 characters) that triggered the workflow.                                                                  | `ffac537e`                |


### Default Environment Variables exposed by GitHub

For a full list of default environment variables exposed by GitHub see [https://help.github.com/en/actions/configuring-and-managing-workflows/using-environment-variables#default-environment-variables](https://help.github.com/en/actions/configuring-and-managing-workflows/using-environment-variables#default-environment-variables).

| Environment Variable Name | Description                                                                                                                                 | Example value                                 |
|---------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| `GITHUB_ACTOR`            | The name of the person or app that initiated the workflow.                                                                                  | `octocat`                                     |
| `GITHUB_REPOSITORY`       | The owner and repository name.                                                                                                              | `FranzDiebold/github-env-vars-action`         |
| `GITHUB_SHA`              | The commit SHA that triggered the workflow.                                                                                                 | `ffac537e6cbbf934b08745a378932722df287a53`    |
| `GITHUB_REF`              | The branch or tag ref that triggered the workflow. If neither a branch or tag is available for the event type, the variable will not exist. | `refs/heads/feature-branch-1`                 |

## Example usage

```yaml
steps:
  - uses: franzdiebold/github-env-vars-action@v1.0.0
  - name: Print environment variables
    run: |
      echo "GITHUB_REPOSITORY_OWNER=$GITHUB_REPOSITORY_OWNER"
      echo "GITHUB_REPOSITORY_NAME=$GITHUB_REPOSITORY_NAME"
      echo "GITHUB_REF_NAME=$GITHUB_REF_NAME"
      echo "GITHUB_SHA_SHORT=$GITHUB_SHA_SHORT"
```
