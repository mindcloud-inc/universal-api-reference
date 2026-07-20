# Get Build Upload Link with E2B

Retrieves a build upload link from E2B.

## Endpoint

- **Method:** `GET`
- **Path:** `/templates/{templateID}/files/{hash}`
- **Base URL:** `https://api.e2b.app`
- **Official documentation:** [Get Build Upload Link](https://e2b.dev/docs/api-reference/templates/get-build-upload-link)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `hash` | path | `string` | yes | Hash of the tar file containing build layer files. |
| `templateID` | path | `string` | yes | Identifier of the template. |
