# List Customers with Metronome

Retrieves customers from Metronome.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/customers`
- **Base URL:** `https://api.metronome.com`
- **Official documentation:** [List Customers](https://docs.metronome.com/api-reference/customers/list-customers)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ingest_alias` | query | `string` | no | Filter the customer list by ingest alias. |
| `customer_ids[]` | query | `array<string>` | no | Filter the customer list by customer ID. Send multiple values as a array. |
| `only_archived` | query | `boolean` | no | Only return archived customers. |
| `salesforce_account_ids[]` | query | `array<string>` | no | Filter the customer list by Salesforce account ID. Send multiple values as a array. |
