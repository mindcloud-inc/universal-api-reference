# Create a new configuration group with Qase

Creates a new configuration group in Qase.

## Endpoint

- **Method:** `POST`
- **Path:** `/configuration/:code/group`
- **Base URL:** `https://api.qase.io/v1`
- **Official documentation:** [Create a new configuration group](https://developers.qase.io/reference/get-projects)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `code` | path | `string` | yes | Code of project, where to search entities. |
| `title` | body | `string` | yes | Required request field title. |
