# Corporate Merch: Cancel Order

Cancels an existing order in Corporate Merch.

```
DELETE https://connect.mindcloud.co/v1/universal/corporateMerch/latest/actions/cancel-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Corporate Merch `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/corporateMerch/latest/actions/cancel-order?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/corporateMerch/latest/actions/cancel-order?${params}`, {
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
      "id": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Corporate Merch API, this operation is `POST /v2/orders/{id}/cancel` (base URL `https://api.corporatemerch.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/cancel-order.md) for the provider-specific parameters and requirements.

