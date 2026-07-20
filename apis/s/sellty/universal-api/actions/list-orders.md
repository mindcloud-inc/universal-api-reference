# Sellty: List Orders



```
GET https://connect.mindcloud.co/v1/universal/sellty/latest/actions/list-orders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sellty `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sellty/latest/actions/list-orders?connectionId=$CONNECTION_ID&limit=25&offset=0&timestamp=2022-10-10%2010%3A10%3A10" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "timestamp": "2022-10-10 10:10:10"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sellty/latest/actions/list-orders?${params}`, {
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
| `timestamp` | string | yes | Required by the Sellty API at runtime. Start date/time for returned orders, for example 2022-10-10 or 2022-10-10 10:10:10. Example: `2022-10-10 10:10:10`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {}
      ],
      "links": {},
      "meta": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> | Order records. |
| `links` | object | Pagination links. |
| `meta` | object | Pagination metadata. |

## Native endpoint

Through the native Sellty API, this operation is `POST /seller/api/v-1-0/get-orders` (base URL `https://my.sellty.ru`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-orders.md) for the provider-specific parameters and requirements.

