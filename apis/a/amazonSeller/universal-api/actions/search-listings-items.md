# Amazon Seller: Search Listings Items

Finds listings items in Amazon Seller.

```
GET https://connect.mindcloud.co/v1/universal/amazonSeller/latest/actions/search-listings-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Amazon Seller `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/amazonSeller/latest/actions/search-listings-items?connectionId=$CONNECTION_ID&limit=25&offset=0&marketplaceIds=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "marketplaceIds": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/amazonSeller/latest/actions/search-listings-items?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `includedData` | list<string> | no | A comma-delimited list of datasets that you want to include in the response. Default: `summaries` - summaries Summary details for the listing item. - attributes A JSON object that contains structured listing item attribute data, keyed by attribute name. - issues Issues that are associated with the listing item. - offers Current offers for the listing item. - fulfillmentAvailability Fulfillment availability details for the listing item. - procurement Vendor procurement details for the listing item. - relationships Relationship details for a listing item (for example, variations). - productTypes Product types associated with a listing item. Accepts multiple values as an array. |
| `marketplaceIds` | list<string> | yes | A comma-delimited list of Amazon marketplace identifiers for the request. ( max length ≤ 1 ) |
| `identifiersType` | list<string> | no | A type of product identifiers that you can use to search for listings items. Note: This is required when `identifiers` is provided. |
| `identifiers` | string | no | A comma-delimited list of product identifiers that you can use to search for listings items. ( max length ≤ 20 ) Note: This is required when you specify `identifiersType` You cannot use 'identifiers' if you specify `variationParentSku` or `packageHierarchySku`. Accepts multiple values as an array. |
| `variationParentSKU` | string | no | Filters results to include listing items that are variation children of the specified SKU. Note: You cannot use `variationParentSku` if you include `identifiers` or `packageHierarchySku` in your request. |
| `packageHierarchySku` | string | no | Filter results to include listing items that contain or are contained by the specified SKU. Note: You cannot use `packageHierarchySku` if you include `identifiers` or `variationParentSku` in your request. |
| `withIssueSeverity` | list<string> | no | Filter results to include only listing items that have issues that match one or more of the specified severity levels. - ERROR Indicates that an issue has occurred, which prevented the submission from processing. For example, a validation error. - WARNING Indicates an issue has occurred that should be reviewed, but it has not prevented the submission from processing. |
| `withStatus` | list<string> | no | Filter results to include only listing items that have the specified status. - BUYABLE The listings item that shoppers can purchase. This status does not apply to vendor listings. - DISCOVERABLE The listings item is visible to shoppers. |
| `withoutStatus` | list<string> | no | Filter results to include only listing items that don't contain the specified statuses. - BUYABLE The listings item can be purchased by shoppers. This status does not apply to vendor listings. - DISCOVERABLE The listings item is visible to shoppers. |
| `createdAfter` | string | no | A date-time that is used to filter listing items. The response includes listings items that were created at or after this time. Values are in ISO 8601 date-time format. |
| `createdBefore` | string | no | A date-time that is used to filter listing items. The response includes listings items that were created at or before this time. Values are in ISO 8601 date-time format. |
| `lastUpdatedAfter` | string | no | A date-time that is used to filter listing items. The response includes listings items that were last updated at or after this time. Values are in ISO 8601 date-time format. |
| `lastUpdatedBefore` | string | no | A date-time that is used to filter listing items. The response includes listings items that were last updated at or before this time. Values are in ISO 8601 date-time format. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `issueLocale` | string | no | A locale that is used to localize issues. When not provided, the default language code of the first marketplace is used. Examples: "en_US", "fr_CA", "fr_FR". When a localization is not available in the specified locale, localized messages default to "en_US". |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Amazon Seller API returns.

## Native endpoint

Through the native Amazon Seller API, this operation is `GET listings/2021-08-01/items/{{credentials.sellerID}}` (base URL `https://{{credentials.environment}}-{{credentials.region}}.amazon.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-listings-items.md) for the provider-specific parameters and requirements.

