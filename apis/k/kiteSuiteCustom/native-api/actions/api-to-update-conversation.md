# Api to update conversation with Kite Suite

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v1/conversation/:id`
- **Base URL:** `https://api.kitesuite.com`
- **Official documentation:** [Api to update conversation](https://api.kitesuite.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `object` | yes | Request body |
| `id` | path | `string` | no | conversation Id |
| `name` | body | `string` | yes | — |
| `memberId` | body | `string` | yes | — |
