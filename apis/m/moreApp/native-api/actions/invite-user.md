# Invite User with MoreApp

Invites a user to MoreApp.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/customers/{{customerId}}/invites`
- **Base URL:** `https://api.moreapp.com`
- **Official documentation:** [Invite User](https://docs.moreapp.com/docs/developer-docs/b91036c4f16dd-invite-user)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerId` | path | `number` | yes | MoreApp customer identifier. |
| `emailAddress` | body | `string` | yes | Email address to invite. |
| `language` | body | `string` | yes | Invite language code. |
