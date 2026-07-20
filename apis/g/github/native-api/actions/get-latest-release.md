# Get Latest Release with GitHub

Retrieves the latest published release from a GitHub repository.

## Endpoint

- **Method:** `GET`
- **Path:** `/repos/:owner/:repo/releases/latest`
- **Base URL:** `https://api.github.com`
- **Official documentation:** [Get Latest Release](https://docs.github.com/en/rest/releases/releases#get-the-latest-release)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `owner` | path | `string` | yes | The account owner of the repository. The name is not case sensitive. |
| `repo` | path | `string` | yes | The name of the repository without the .git extension. The name is not case sensitive. |
