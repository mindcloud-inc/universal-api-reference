# SquareSpace: List Inventory

Retrieves inventory from Squarespace.

```
GET https://connect.mindcloud.co/v1/universal/squareSpace/latest/actions/list-inventory
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SquareSpace `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/squareSpace/latest/actions/list-inventory?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/squareSpace/latest/actions/list-inventory?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "inventory": [
        {}
      ],
      "pagination": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `inventory` | array<object> | Inventory rows. |
| `pagination` | object | Pagination metadata. |

## Native endpoint

Through the native SquareSpace API, this operation is `GET /1.0/commerce/inventory` (base URL `https://api.squarespace.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-inventory.md) for the provider-specific parameters and requirements.

