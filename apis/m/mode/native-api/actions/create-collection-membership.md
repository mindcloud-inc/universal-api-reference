# Create Collection Membership with Mode

Add a member to a collection in a Mode workspace.

## Endpoint

- **Method:** `POST`
- **Path:** `/spaces/[:space]/memberships`
- **Base URL:** `https://app.mode.com/api/{workspace}`
- **Official documentation:** [Create Collection Membership](https://mode.com/developer/api-reference/management/space-memberships/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `space` | path | `string` | yes | Mode collection token. |
| `membership` | body | `object` | yes | Collection membership fields to create. |
