# List Credentials with Verix

Retrieves credentials from your Verix account.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/credentials`
- **Base URL:** `https://api.verix.io`
- **Official documentation:** [List Credentials](https://docs.verix.io/verifiable_credentials_apis/)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page_size` | query | `number` | no | Number of credentials to return per page. |
| `page_number` | query | `number` | no | 1-based page number to retrieve. |
| `name` | query | `string` | no | Approximate credential name to search. |
| `group_id` | query | `number` | no | Filter credentials by Verix group ID. |
| `external_id` | query | `string` | no | Filter credentials by recipient external ID. |
