# List Team Members with SeekTable

Retrieves team members from a SeekTable account.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/account/:id/team/member`
- **Base URL:** `https://www.seektable.com`
- **Official documentation:** [List Team Members](https://www.seektable.com/help/self-hosted-admin-accounts-api)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | query | `string` | no | Optional login email to filter the team-member list. |
| `id` | path | `number` | yes | ID of the user account that owns the team. |
