# HubSpot: Search Products

Finds products in HubSpot.

```
GET https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/search-products
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HubSpot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/search-products?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/search-products?${params}`, {
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
| `query` | string | no | Full-text search string applied to the default searchable product properties. Example: `a`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `limit` | number | no | Maximum number of records to return in this search page. Example: `10`. |
| `after` | string | no | Paging cursor for the next search page. Example: `next-cursor`. |
| `properties[]` | array<string> | no | Properties to include in each returned product record. |
| `sorts[]` | array<string> | no | Sort clauses to apply to the search results. |
| `filterGroups` | object<object> | no | Provide the full HubSpot filterGroups array, for example [{"filters":[{"propertyName":"hs_object_id","operator":"EQ","value":"123"}]}]. |
| `filterGroups[].filters[]` | array<object> | no | Filters combined with AND semantics inside a filter group. |
| `filterGroups[].filters[].propertyName` | string | no | The product property name to filter on. Example: `name`. |
| `filterGroups[].filters[].operator` | list<string> | no | The comparison operator to use for the filter. One of: `BETWEEN`, `CONTAINS_TOKEN`, `EQ`, `GT`, `GTE`, `HAS_PROPERTY`, `IN`, `LT`, `LTE`, `NEQ`, `NOT_CONTAINS_TOKEN`, `NOT_HAS_PROPERTY`, `NOT_IN`. |
| `filterGroups[].filters[].value` | string | no | Single comparison value for the filter. Example: `widget`. |
| `filterGroups[].filters[].values[]` | array<string> | no | Multiple comparison values for IN and NOT_IN filters. |
| `filterGroups[].filters[].highValue` | string | no | Upper bound value for BETWEEN filters. Example: `z`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "properties": {},
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean | Whether the product is archived. |
| `createdAt` | date | When the product was created. |
| `id` | string | The product record ID. |
| `properties` | object | The returned product properties. |
| `updatedAt` | date | When the product was last updated. |
| `url` | string | The HubSpot product URL. |

## Native endpoint

Through the native HubSpot API, this operation is `POST crm/v3/objects/products/search` (base URL `https://api.hubapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-products.md) for the provider-specific parameters and requirements.

