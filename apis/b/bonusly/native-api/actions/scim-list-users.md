# SCIM List Users with Bonusly

Retrieves SCIM users from Bonusly.

## Endpoint

- **Method:** `GET`
- **Path:** `https://bonus.ly/api/scim11/Users`
- **Base URL:** `https://bonus.ly/api/v1`
- **Official documentation:** [SCIM List Users](https://docs.bonus.ly/reference/list-users)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `count` | query | `string` | no | Number of SCIM users to return. |
| `startIndex` | query | `string` | no | 1-based starting index for SCIM pagination. |
