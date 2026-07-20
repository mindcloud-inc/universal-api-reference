# SalesDrive: List Delivery Methods

Retrieves available delivery methods from SalesDrive.

```
GET https://connect.mindcloud.co/v1/universal/salesDrive/latest/actions/list-delivery-methods
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SalesDrive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/salesDrive/latest/actions/list-delivery-methods?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/salesDrive/latest/actions/list-delivery-methods?${params}`, {
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
      "id": 1,
      "name": "Ava Chen",
      "parameter": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `name` | string |  |
| `parameter` | string |  |

## Native endpoint

Through the native SalesDrive API, this operation is `GET /api/delivery-methods/` (base URL `https://{{credentials.account}}.salesdrive.me`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-delivery-methods.md) for the provider-specific parameters and requirements.

