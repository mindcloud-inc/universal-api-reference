# Create a new milestone with Qase

Creates a new milestone in Qase.

## Endpoint

- **Method:** `POST`
- **Path:** `/milestone/:code`
- **Base URL:** `https://api.qase.io/v1`
- **Official documentation:** [Create a new milestone](https://developers.qase.io/reference/get-projects)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `code` | path | `string` | yes | Code of project, where to search entities. |
| `title` | body | `string` | yes | Required request field title. |
