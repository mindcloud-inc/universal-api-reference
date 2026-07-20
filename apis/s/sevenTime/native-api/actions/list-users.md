# List Users with Seven Time

Retrieves users from a Seven Time workspace.

## Endpoint

- **Method:** `GET`
- **Path:** `/users`
- **Base URL:** `https://app.seventime.se/api/2`
- **Official documentation:** [List Users](https://docs.seventime.se/#get-users)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `name` | query | `string` | no |
| `personNumber` | query | `string` | no |
| `department` | query | `string` | no |
| `userRole` | query | `string` | no |
| `isActive` | query | `boolean` | no |
| `isActivated` | query | `boolean` | no |
| `defaultSalaryType` | query | `string` | no |
