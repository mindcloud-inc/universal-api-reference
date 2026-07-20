# Recommend Items to User with Recombee

Retrieves item recommendations for a user from Recombee.

## Endpoint

- **Method:** `POST`
- **Path:** `/recomms/users/:userId/items/`
- **Base URL:** `https://rapi.recombee.com/{databaseId}`
- **Official documentation:** [Recommend Items to User](https://docs.recombee.com/api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `count` | body | `string` | no |
| `userId` | path | `string` | yes |
