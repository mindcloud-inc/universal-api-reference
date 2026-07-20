# List Campaigns with Veedea

Retrieves all campaign records from Veedea.

## Endpoint

- **Method:** `GET`
- **Path:** `/getcampaign`
- **Base URL:** `https://veedea.com/api`
- **Official documentation:** [List Campaigns](https://veedea.com/api/doc)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `token` | query | `string` | yes | Auth token returned by the Veedea authentication endpoint. |
