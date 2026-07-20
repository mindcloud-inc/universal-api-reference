# List Users with Engage

Retrieves users from Engage with optional email filtering.

## Endpoint

- **Method:** `GET`
- **Path:** `/users`
- **Base URL:** `https://api.engage.so/v1`
- **Official documentation:** [List Users](https://docs.engage.so/en-us/a/62bbdd015bfea4dca4834042-users#list-users)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | query | `string` | no | Filter the results to users with this email address. |
