# List Team Groups with SeekTable

Retrieves team groups from a SeekTable account.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/account/:id/team/group`
- **Base URL:** `https://www.seektable.com`
- **Official documentation:** [List Team Groups](https://www.seektable.com/help/self-hosted-admin-accounts-api)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | ID of the user account that owns the team. |
