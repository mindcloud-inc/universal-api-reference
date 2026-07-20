# List Partner Property Listing Statuses with EasyBroker

Retrieves partner property listing statuses from EasyBroker.

## Endpoint

- **Method:** `GET`
- **Path:** `/integration_partners/listing_statuses`
- **Base URL:** `https://api.easybroker.com/v1`
- **Official documentation:** [List Partner Property Listing Statuses](https://dev.easybroker.com/reference/get_listing-statuses-1)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search[agency_id]` | query | `string` | no | Filter listings from one specific agency. |
| `search[published]` | query | `boolean` | no | Filter published or unpublished properties. |
