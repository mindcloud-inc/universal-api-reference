# Get Collection Membership with Mode

Get details for a specific membership in a Mode collection.

## Endpoint

- **Method:** `GET`
- **Path:** `/spaces/[:space]/memberships/[:spaceMembership]`
- **Base URL:** `https://app.mode.com/api/{workspace}`
- **Official documentation:** [Get Collection Membership](https://mode.com/developer/api-reference/management/space-memberships/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `space` | path | `string` | yes | Mode collection token. |
| `spaceMembership` | path | `string` | yes | Mode collection membership token. |
