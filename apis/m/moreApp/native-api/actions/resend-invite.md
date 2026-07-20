# Resend Invite with MoreApp

Resends an invite in MoreApp.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/customers/{{customerId}}/invites/{{id}}/resend`
- **Base URL:** `https://api.moreapp.com`
- **Official documentation:** [Resend Invite](https://docs.moreapp.com/docs/developer-docs/7d1ef261253f6-resend-invite)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `customerId` | path | `number` | yes |
| `id` | path | `string` | yes |
