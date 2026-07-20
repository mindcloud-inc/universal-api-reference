# Revoke Invite with MoreApp

Revokes an invite in MoreApp.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/v2/customers/{{customerId}}/invites/{{id}}`
- **Base URL:** `https://api.moreapp.com`
- **Official documentation:** [Revoke Invite](https://docs.moreapp.com/docs/developer-docs/d33c664a81b0b-revoke-invite)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerId` | path | `number` | yes | MoreApp customer identifier. |
| `id` | path | `string` | yes | MoreApp invite identifier. |
