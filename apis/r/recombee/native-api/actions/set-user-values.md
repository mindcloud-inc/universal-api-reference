# Set User Values with Recombee

Updates values for a user in Recombee.

## Endpoint

- **Method:** `POST`
- **Path:** `/users/:userId`
- **Base URL:** `https://rapi.recombee.com/{databaseId}`
- **Official documentation:** [Set User Values](https://docs.recombee.com/api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `cascadeCreate` | query | `string` | no |
| `userId` | path | `string` | yes |
| `values` | body | `object` | yes |
