# List Repository Labels with GitHub

## Endpoint

- **Method:** `GET`
- **Path:** `/repos/:owner/:repo/labels`
- **Base URL:** `https://api.github.com`
- **Official documentation:** [List Repository Labels](https://docs.github.com/en/rest/issues/labels#list-labels-for-a-repository)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `owner` | path | `string` | yes | The account owner of the repository. The name is not case sensitive. |
| `repo` | path | `string` | yes | The name of the repository without the .git extension. The name is not case sensitive. |
| `per_page` | query | `number` | no | The number of results per page (max 100). |
