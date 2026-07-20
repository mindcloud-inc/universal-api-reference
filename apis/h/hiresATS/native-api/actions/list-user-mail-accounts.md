# List User Mail Accounts with 100Hires ATS

Lists a user's mail accounts in 100Hires ATS.

## Endpoint

- **Method:** `GET`
- **Path:** `/users/:id/mail-accounts`
- **Base URL:** `https://api.100hires.com/v2`
- **Official documentation:** [List User Mail Accounts](https://100hires.com/api)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | ID of the user whose mail accounts to list. |
