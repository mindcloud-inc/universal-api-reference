# Merge Users with Engage

Merges one user into another in Engage.

## Endpoint

- **Method:** `POST`
- **Path:** `/users/merge`
- **Base URL:** `https://api.engage.so/v1`
- **Official documentation:** [Merge Users](https://docs.engage.so/en-us/a/62bbdd015bfea4dca4834042-users#merge-users)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `source` | body | `string` | yes | The user ID to merge from. |
| `destination` | body | `string` | yes | The user ID to merge into. |
