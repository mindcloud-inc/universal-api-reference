# Get Listings Item with Amazon Seller

Retrieves a listings item from Amazon Seller.

## Endpoint

- **Method:** `GET`
- **Path:** `listings/2021-08-01/items/{sellerID}/:sku`
- **Base URL:** `https://{environment}-{region}.amazon.com`
- **API:** REST
- **Official documentation:** [Get Listings Item](https://developer-docs.amazon.com/sp-api/reference/getlistingsitem)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `includedData` | query | `list<string>` | no | A comma-delimited list of data sets to include in the response. Default: `summaries`  - summaries	Summary details of the listing item. - attributes	A JSON object containing structured listing item attribute data keyed by attribute name. - issues	The issues associated with the listing item. - offers	The current offers for the listing item. - fulfillmentAvailability	The fulfillment availability details for the listing item. - procurement	Vendor procurement details for the listing item. - relationships	Relationship details for a listing item (for example, variations). - productTypes	Product types that are associated with a listing item. Send multiple values as a string. |
| `marketplaceIds` | query | `list<string>` | yes | The Amazon marketplace identifier for the request. ( max length ≤ 1 ) Maximum length: 0. Send multiple values as a array. |
| `sku` | path | `string` | yes | A selling partner provided identifier for an Amazon listing. |
| `issueLocale` | query | `string` | no | A locale for localization of issues. When not provided, the default language code of the first marketplace is used.  Examples: `en_US`, `fr_CA`, `fr_FR`. Localized messages default to `en_US` when a localization is not available in the specified locale. |
