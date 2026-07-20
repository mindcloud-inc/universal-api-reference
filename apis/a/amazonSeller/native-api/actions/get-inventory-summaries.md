# Get FBA Inventory Summaries (AFN only) with Amazon Seller

Retrieves AFN inventory summaries from Amazon Seller.

## Endpoint

- **Method:** `GET`
- **Path:** `fba/inventory/v1/summaries`
- **Base URL:** `https://{environment}-{region}.amazon.com`
- **API:** REST
- **Official documentation:** [Get FBA Inventory Summaries (AFN only)](https://developer-docs.amazon.com/sp-api/reference/getorders)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `marketplaceIds` | query | `list<string>` | yes | The marketplace ID of the marketplace for which to return inventory summaries. (max: 1x marketplace) Maximum length: 0. |
| `startDateTime` | query | `string` | no | A start date and time - If specified, all inventory summaries that have changed since then are returned. You must specify a date and time that is no earlier than 18 months prior to the date and time when you call the API.  Note: Changes in `inboundWorkingQuantity`, `inboundShippedQuantity` and `inboundReceivingQuantity` are not detected. |
| `sellerSkus` | query | `string` | no | A list of seller SKUs for which to return inventory summaries. You may specify up to 50 SKUs. Maximum length: 50. Send multiple values as a string. |
| `details` | query | `boolean` | no | Toggle on to return inventory summaries with additional summarized inventory details and quantities. Otherwise, returns inventory summaries only (default value). |
| `granularityType` | query | `string` | no | The granularity type for the inventory aggregation level.  Allowed: `Marketplace` |
