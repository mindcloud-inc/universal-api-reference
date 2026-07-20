# Update role in workspace by workspace Id. with Kite Suite

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v1/workspace/member/:id`
- **Base URL:** `https://api.kitesuite.com`
- **Official documentation:** [Update role in workspace by workspace Id.](https://api.kitesuite.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `object` | yes | Request body |
| `id` | path | `string` | no | Member ID |
| `roleID` | body | `string` | yes | — |
