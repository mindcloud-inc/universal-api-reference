# Invite Accounts with Feathery

## Endpoint

- **Method:** `POST`
- **Path:** `/api/account/invite/`
- **Base URL:** `https://api.feathery.io`
- **Official documentation:** [Invite Accounts](https://api-docs.feathery.io/#invite-accounts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accounts[]` | body | `array<object>` | yes | An array of account invite objects. Each object can include email, role, permissions, and user_groups per the Feathery docs. |
