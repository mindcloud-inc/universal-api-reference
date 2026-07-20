# List Leads with Veedea

Retrieves all lead records from Veedea.

## Endpoint

- **Method:** `GET`
- **Path:** `/getleads`
- **Base URL:** `https://veedea.com/api`
- **Official documentation:** [List Leads](https://veedea.com/api/doc)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaign-id` | query | `number` | yes | Campaign ID returned by the Veedea campaigns endpoint. |
| `token` | query | `string` | yes | Auth token returned by the Veedea authentication endpoint. |
