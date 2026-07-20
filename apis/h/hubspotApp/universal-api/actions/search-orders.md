# HubSpot: Search Orders

Finds orders in HubSpot.

```
GET https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/search-orders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HubSpot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/search-orders?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/search-orders?${params}`, {
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
| `query` | string | no | A text query to search order records. |
| `filterGroups` | object<object> | no | Provide the full HubSpot filterGroups array, for example [{"filters":[{"propertyName":"hs_object_id","operator":"EQ","value":"123"}]}]. |
| `filterGroups[].filters[]` | array<object> | no | The filters inside each filter group. |
| `filterGroups[].filters[].propertyName` | string | no | The property to filter on. |
| `filterGroups[].filters[].operator` | list | no | The filter operator. One of: `BETWEEN`, `CONTAINS_TOKEN`, `EQ`, `GT`, `GTE`, `HAS_PROPERTY`, `IN`, `LT`, `LTE`, `NEQ`, `NOT_CONTAINS_TOKEN`, `NOT_HAS_PROPERTY`, `NOT_IN`. |
| `filterGroups[].filters[].value` | string | no | The primary filter value. |
| `filterGroups[].filters[].highValue` | string | no | The high value for range filters. |
| `filterGroups[].filters[].values[]` | array<string> | no | Multiple filter values when supported. |
| `after` | string | no | The paging cursor token. |
| `limit` | number | no | The maximum number of orders to return. |
| `sorts[]` | array<string> | no | Sort expressions for the search results. |
| `properties[]` | array<string> | no | The order properties to include in each result. |

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
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean | Whether the order is archived. |
| `createdAt` | date | When the order was created. |
| `id` | string | The order record ID. |
| `properties` | object | The returned order properties. |
| `updatedAt` | date | When the order was last updated. |

## Native endpoint

Through the native HubSpot API, this operation is `POST crm/v3/objects/orders/search` (base URL `https://api.hubapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-orders.md) for the provider-specific parameters and requirements.

