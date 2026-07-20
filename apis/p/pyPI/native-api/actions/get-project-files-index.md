# Get Project Files Index with PyPI

Retrieves distribution download URLs for a PyPI project.

## Endpoint

- **Method:** `GET`
- **Path:** `/simple/:project/`
- **Base URL:** `https://pypi.org`
- **Official documentation:** [Get Project Files Index](https://docs.pypi.org/api/index-api/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/vnd.pypi.simple.v1+json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project` | path | `string` | yes | The normalized PyPI project name whose file index you want to list. |
