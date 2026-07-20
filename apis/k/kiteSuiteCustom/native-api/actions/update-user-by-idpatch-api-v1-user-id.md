# Update User By ID with Kite Suite

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v1/user/:id`
- **Base URL:** `https://api.kitesuite.com`
- **Official documentation:** [Update User By ID](https://api.kitesuite.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | user ID |
| `body` | body | `object` | yes | Request body |
| `fullName` | body | `string` | yes | — |
| `email` | body | `string` | yes | — |
