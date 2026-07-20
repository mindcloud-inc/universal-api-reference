# List Client Contacts with EenvoudigFactureren

Retrieves client contacts from EenvoudigFactureren.

## Endpoint

- **Method:** `GET`
- **Path:** `/clients/:client_id/contacts`
- **Base URL:** `https://eenvoudigfactureren.be/api/v1`
- **Official documentation:** [List Client Contacts](https://help.eenvoudigfactureren.be/support/solutions/articles/101000381976-api-klanten)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `client_id` | path | `string` | yes | EenvoudigFactureren client ID. |
