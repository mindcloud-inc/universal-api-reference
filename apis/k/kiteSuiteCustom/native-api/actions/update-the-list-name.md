# Update the ListName with Kite Suite

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v1/list/:id`
- **Base URL:** `https://api.kitesuite.com`
- **Official documentation:** [Update the ListName](https://api.kitesuite.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `object` | yes | Request body |
| `id` | path | `string` | no | listID |
| `listName` | body | `string` | yes | — |
| `status` | body | `string` | yes | — |
