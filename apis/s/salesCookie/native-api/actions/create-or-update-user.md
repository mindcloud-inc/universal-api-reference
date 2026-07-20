# Create Or Update User with Sales Cookie

Creates or updates a user in Sales Cookie by email address.

## Endpoint

- **Method:** `POST`
- **Path:** `/Api/SetUser`
- **Base URL:** `https://salescookie.com/app`
- **Official documentation:** [Create Or Update User](https://support2.salescookie.com/portal/en/kb/articles/kb-how-can-i-programmatically-create-or-update-users)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `emailAddress` | body | `string` | yes | User email address used to create or update the user. |
| `role` | body | `string` | yes | Workspace role. Valid values include FullAdmin, LimitedAdmin, Participant, and Deactivated. |
| `firstName` | body | `string` | no | — |
| `lastName` | body | `string` | no | — |
| `tags` | body | `string` | no | Optional pipe-delimited tags. |
| `aliases` | body | `string` | no | Optional pipe-delimited aliases. |
