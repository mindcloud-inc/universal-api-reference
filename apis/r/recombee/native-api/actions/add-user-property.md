# Add User Property with Recombee

Creates a new user property in Recombee.

## Endpoint

- **Method:** `PUT`
- **Path:** `/users/properties/:propertyName`
- **Base URL:** `https://rapi.recombee.com/{databaseId}`
- **Official documentation:** [Add User Property](https://docs.recombee.com/api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `propertyName` | path | `string` | yes |
| `type` | query | `string` | yes |
