# Search Listings Items with Amazon Seller

Finds listings items in Amazon Seller.

## Endpoint

- **Method:** `GET`
- **Path:** `listings/2021-08-01/items/{sellerID}`
- **Base URL:** `https://{environment}-{region}.amazon.com`
- **API:** pageSize / pageToken
- **Official documentation:** [Search Listings Items](https://developer-docs.amazon.com/sp-api/reference/searchlistingsitems)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `includedData` | query | `list<string>` | no | A comma-delimited list of datasets that you want to include in the response.  Default: `summaries`  - summaries	Summary details for the listing item. - attributes	A JSON object that contains structured listing item attribute data, keyed by attribute name. - issues	Issues that are associated with the listing item. - offers	Current offers for the listing item. - fulfillmentAvailability	Fulfillment availability details for the listing item. - procurement	Vendor procurement details for the listing item. - relationships	Relationship details for a listing item (for example, variations). - productTypes	Product types associated with a listing item. Send multiple values as a array. |
| `marketplaceIds` | query | `list<string>` | yes | A comma-delimited list of Amazon marketplace identifiers for the request. ( max length ≤ 1 ) Maximum length: 0. |
| `identifiersType` | query | `list<string>` | no | A type of product identifiers that you can use to search for listings items.   Note: This is required when `identifiers` is provided. |
| `identifiers` | query | `string` | no | A comma-delimited list of product identifiers that you can use to search for listings items. ( max length ≤ 20 )  Note: This is required when you specify `identifiersType` You cannot use 'identifiers' if you specify `variationParentSku` or `packageHierarchySku`. Maximum length: 20. Send multiple values as a array. |
| `variationParentSKU` | query | `string` | no | Filters results to include listing items that are variation children of the specified SKU.  Note: You cannot use `variationParentSku` if you include `identifiers` or `packageHierarchySku` in your request. |
| `packageHierarchySku` | query | `string` | no | Filter results to include listing items that contain or are contained by the specified SKU.  Note: You cannot use `packageHierarchySku` if you include `identifiers` or `variationParentSku` in your request. |
| `withIssueSeverity` | query | `list<string>` | no | Filter results to include only listing items that have issues that match one or more of the specified severity levels.  - ERROR	Indicates that an issue has occurred, which prevented the submission from processing. For example, a validation error. - WARNING	Indicates an issue has occurred that should be reviewed, but it has not prevented the submission from processing. |
| `withStatus` | query | `list<string>` | no | Filter results to include only listing items that have the specified status.  - BUYABLE	The listings item that shoppers can purchase. This status does not apply to vendor listings. - DISCOVERABLE	The listings item is visible to shoppers. |
| `withoutStatus` | query | `list<string>` | no | Filter results to include only listing items that don't contain the specified statuses.  - BUYABLE	The listings item can be purchased by shoppers. This status does not apply to vendor listings. - DISCOVERABLE	The listings item is visible to shoppers. |
| `createdAfter` | query | `string` | no | A date-time that is used to filter listing items. The response includes listings items that were created at or after this time.  Values are in ISO 8601 date-time format. |
| `createdBefore` | query | `string` | no | A date-time that is used to filter listing items. The response includes listings items that were created at or before this time.  Values are in ISO 8601 date-time format. |
| `lastUpdatedAfter` | query | `string` | no | A date-time that is used to filter listing items. The response includes listings items that were last updated at or after this time.  Values are in ISO 8601 date-time format. |
| `lastUpdatedBefore` | query | `string` | no | A date-time that is used to filter listing items. The response includes listings items that were last updated at or before this time.  Values are in ISO 8601 date-time format. |
| `issueLocale` | query | `string` | no | A locale that is used to localize issues. When not provided, the default language code of the first marketplace is used.  Examples: "en_US", "fr_CA", "fr_FR".  When a localization is not available in the specified locale, localized messages default to "en_US". |
