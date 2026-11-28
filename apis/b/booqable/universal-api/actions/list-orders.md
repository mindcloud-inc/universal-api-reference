# Booqable: List Orders

Retrieves order records from Booqable.

```
GET https://connect.mindcloud.co/v1/universal/booqable/latest/actions/list-orders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Booqable `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/booqable/latest/actions/list-orders?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/booqable/latest/actions/list-orders?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fieldsOrders` | string | no | Comma-separated order fields to include instead of the default fields. Example: `created_at,updated_at,number`. |
| `include` | string | no | Comma-separated relationships to sideload. Example: `customer,coupon,start_location`. |
| `filter` | string | no | Booqable filters as a JSON object, for example {"archived":{"eq":false}}. Example: `[object Object]`. |
| `metaTotal` | string<string> | no | Aggregations to include in meta.total. Accepts multiple values as an array. Example: `count`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {},
      "id": "string",
      "relationships": {},
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes` | object | Order attributes object. |
| `id` | string | Order UUID. |
| `relationships` | object | Order relationships object. |
| `type` | string | Resource type. |

## Native endpoint

Through the native Booqable API, this operation is `GET /orders` (base URL `https://{{credentials.companySlug}}.booqable.com/api/4`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-orders.md) for the provider-specific parameters and requirements.

