# Create Account Invite For User with Frontegg

Creates an account invitation for a user in Frontegg.

## Endpoint

- **Method:** `POST`
- **Path:** `/identity/resources/tenants/invites/v1/user`
- **Base URL:** `https://api.frontegg.com`
- **Official documentation:** [Create Account Invite For User](https://developers.frontegg.com/ciam/api/identity/account-invitations)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `expiresInMinutes` | body | `number` | yes | Invitation expiration time in minutes. |
| `shouldSendEmail` | body | `boolean` | yes | Whether to send the invitation email. |
