# List Sandboxes with E2B

Retrieves a list of running sandboxes from E2B.

## Endpoint

- **Method:** `GET`
- **Path:** `/sandboxes`
- **Base URL:** `https://api.e2b.app`
- **Official documentation:** [List Sandboxes](https://e2b.dev/docs/api-reference/sandboxes/list-sandboxes)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `metadata` | query | `string` | no | Optional URL-encoded metadata query used to filter sandboxes, such as user=abc&app=prod. |
