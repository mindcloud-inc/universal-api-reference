# List Clients with Clientary

Retrieves clients from your Clientary account.

## Endpoint

- **Method:** `GET`
- **Path:** `/clients`
- **Base URL:** `https://{subdomain}.clientary.com/api/v2`
- **Official documentation:** [List Clients](https://www.clientary.com/api/clients)

## Capabilities

This operation supports [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `updated_since` | query | `string` | no | Return only clients updated after this timestamp. |
