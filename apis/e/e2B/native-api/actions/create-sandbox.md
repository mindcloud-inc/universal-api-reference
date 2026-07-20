# Create Sandbox with E2B

Creates a sandbox from a template in E2B.

## Endpoint

- **Method:** `POST`
- **Path:** `/sandboxes`
- **Base URL:** `https://api.e2b.app`
- **Official documentation:** [Create Sandbox](https://e2b.dev/docs/api-reference/sandboxes/create-sandbox)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `templateID` | body | `string` | yes | Identifier of the required template. |
