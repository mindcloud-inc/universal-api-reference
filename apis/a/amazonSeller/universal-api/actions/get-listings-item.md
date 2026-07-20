# Amazon Seller: Get Listings Item

Retrieves a listings item from Amazon Seller.

```
GET https://connect.mindcloud.co/v1/universal/amazonSeller/latest/actions/get-listings-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Amazon Seller `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/amazonSeller/latest/actions/get-listings-item?connectionId=$CONNECTION_ID&marketplaceIds=string&sku=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "marketplaceIds": "string",
  "sku": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/amazonSeller/latest/actions/get-listings-item?${params}`, {
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
| `includedData` | list<string> | no | A comma-delimited list of data sets to include in the response. Default: `summaries` - summaries Summary details of the listing item. - attributes A JSON object containing structured listing item attribute data keyed by attribute name. - issues The issues associated with the listing item. - offers The current offers for the listing item. - fulfillmentAvailability The fulfillment availability details for the listing item. - procurement Vendor procurement details for the listing item. - relationships Relationship details for a listing item (for example, variations). - productTypes Product types that are associated with a listing item. Accepts multiple values in one string. |
| `marketplaceIds` | list<string> | yes | The Amazon marketplace identifier for the request. ( max length ≤ 1 ) Accepts multiple values as an array. |
| `sku` | string | yes | A selling partner provided identifier for an Amazon listing. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `issueLocale` | string | no | A locale for localization of issues. When not provided, the default language code of the first marketplace is used. Examples: `en_US`, `fr_CA`, `fr_FR`. Localized messages default to `en_US` when a localization is not available in the specified locale. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Amazon Seller API returns.

## Native endpoint

Through the native Amazon Seller API, this operation is `GET listings/2021-08-01/items/{{credentials.sellerID}}/:sku` (base URL `https://{{credentials.environment}}-{{credentials.region}}.amazon.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-listings-item.md) for the provider-specific parameters and requirements.

