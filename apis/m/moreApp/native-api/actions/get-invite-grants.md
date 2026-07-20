# Get Invite Grants with MoreApp

Retrieves grants for an invite from MoreApp.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/customers/{{customerId}}/invites/{{id}}/grants`
- **Base URL:** `https://api.moreapp.com`
- **Official documentation:** [Get Invite Grants](https://docs.moreapp.com/docs/developer-docs/9606bfeae6e60-get-grants-for-invite)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `customerId` | path | `number` | yes |
| `id` | path | `string` | yes |
