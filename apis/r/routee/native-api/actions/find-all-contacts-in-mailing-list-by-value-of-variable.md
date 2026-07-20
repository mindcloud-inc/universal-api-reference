# Find all contacts in mailing list by value of variable with Routee

Finds all contacts in mailing list by value of variable in Routee.

## Endpoint

- **Method:** `GET`
- **Path:** `/addressbooks/:id/variables/:variableName/:searchValue`
- **Base URL:** `https://connect.routee.net`
- **Official documentation:** [Find all contacts in mailing list by value of variable](https://docs.routee.net/reference/find-all-contacts-in-mailing-list-by-value-of-variable)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | the ID of the mailing list |
| `variableName` | path | `string` | yes | name of variable |
| `searchValue` | path | `string` | yes | value of variable |
