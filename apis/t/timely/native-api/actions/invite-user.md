# Invite User with Timely

Invites a user to Timely.

## Endpoint

- **Method:** `POST`
- **Path:** `/1.1/{account_id}/users`
- **Base URL:** `https://api.timelyapp.com`
- **Official documentation:** [Invite User](https://developer.timely.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account_id` | path | `number` | yes | Workspace id |
| `user` | body | `object` | yes | — |
