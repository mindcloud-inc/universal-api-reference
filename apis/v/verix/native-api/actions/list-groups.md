# List Groups with Verix

Retrieves credential groups from your Verix account.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/credentials/groups`
- **Base URL:** `https://api.verix.io`
- **Official documentation:** [List Groups](https://docs.verix.io/verifiable_credentials_apis/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page_number` | query | `string` | no | 1-based page number to retrieve. |
| `page_size` | query | `string` | no | Number of groups to return per page. Verix defaults to 10. |
