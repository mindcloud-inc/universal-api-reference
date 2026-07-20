# Update Label with Rossum

Updates a label in Rossum.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/labels/:labelID`
- **Base URL:** `https://mindcloud.rossum.app/api/v1`
- **Official documentation:** [Update Label](https://rossum.app/api/docs/openapi/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `labelID` | path | `number` | yes | Rossum label ID. |
| `name` | body | `string` | no | Updated label name. |
