# List Accounts with Recurly

## Endpoint

- **Method:** `GET`
- **Path:** `/accounts`
- **Base URL:** `https://v3.recurly.com`
- **Official documentation:** [List Accounts](https://recurly.com/developers/api/v2021-02-25/#operation/list_accounts)

## Capabilities

This operation supports [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `begin_time` | query | `string` | no | Only return accounts created or updated on or after this timestamp. |
| `email` | query | `string` | no | Filter accounts by email address. |
| `end_time` | query | `string` | no | Only return accounts created or updated before this timestamp. |
| `ids` | query | `string` | no | Filter by one or more account IDs. |
| `subscriber` | query | `boolean` | no | Only return accounts that currently have or had subscriptions. |
