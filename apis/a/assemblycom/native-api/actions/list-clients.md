# List Clients with Assembly.com

Retrieves clients from Assembly.com.

## Endpoint

- **Method:** `GET`
- **Path:** `/clients`
- **Base URL:** `https://api.assembly.com/v1`
- **Official documentation:** [List Clients](https://docs.assembly.com/reference/list-clients)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `companyId` | query | `string` | no | Any of the company IDs of the client user(s) to query for. |
| `email` | query | `string` | no | The email of the client user to query for (exact match, case-sensitive). |
| `familyName` | query | `string` | no | The family name of the client user(s) to query for (exact match, case-sensitive). |
| `givenName` | query | `string` | no | The given name of the client user(s) to query for (exact match, case-sensitive). |
