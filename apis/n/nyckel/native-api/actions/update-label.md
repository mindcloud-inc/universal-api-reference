# Update Label with Nyckel

Updates an existing label in Nyckel.

## Endpoint

- **Method:** `PUT`
- **Path:** `/functions/:functionId/labels/:labelId`
- **Base URL:** `https://www.nyckel.com/v1`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `functionId` | path | `string` | yes | Nyckel function identifier. |
| `labelId` | path | `string` | yes | Nyckel label identifier. |
| `name` | body | `string` | yes | Updated label name. |
| `description` | body | `string` | no | Updated label description. |
| `metadata` | body | `object` | no | Updated label metadata object. |
