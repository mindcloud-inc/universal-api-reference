# List User Accounts with SeekTable

Retrieves user accounts from a SeekTable installation.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/account`
- **Base URL:** `https://www.seektable.com`
- **Official documentation:** [List User Accounts](https://www.seektable.com/help/self-hosted-admin-accounts-api)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | query | `string` | no | Optional login email to filter the user-account list. |
