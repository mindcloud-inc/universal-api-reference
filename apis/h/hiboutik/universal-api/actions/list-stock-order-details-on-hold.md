# Hiboutik: List Stock Order Details on Hold

Retrieves on-hold stock order details from Hiboutik.

```
GET https://connect.mindcloud.co/v1/universal/hiboutik/latest/actions/list-stock-order-details-on-hold
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hiboutik `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hiboutik/latest/actions/list-stock-order-details-on-hold?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hiboutik/latest/actions/list-stock-order-details-on-hold?${params}`, {
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
      "inventoryInputId": 1,
      "productId": 1,
      "quantity": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `inventoryInputId` | number |  |
| `productId` | number |  |
| `quantity` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Hiboutik API, this operation is `GET /inventory_inputs_on_hold/` (base URL `https://mindcloudhiboutik20260402.hiboutik.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-stock-order-details-on-hold.md) for the provider-specific parameters and requirements.

