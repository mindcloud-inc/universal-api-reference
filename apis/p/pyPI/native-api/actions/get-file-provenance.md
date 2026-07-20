# Get File Provenance with PyPI

Retrieves provenance for a PyPI distribution file.

## Endpoint

- **Method:** `GET`
- **Path:** `/integrity/:project/:version/:filename/provenance`
- **Base URL:** `https://pypi.org`
- **Official documentation:** [Get File Provenance](https://docs.pypi.org/api/integrity/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/vnd.pypi.integrity.v1+json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project` | path | `string` | yes | The normalized PyPI project name. |
| `version` | path | `string` | yes | The release version that owns the uploaded file. |
| `filename` | path | `string` | yes | The exact distribution filename, including extension. |
