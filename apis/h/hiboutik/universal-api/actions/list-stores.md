# Hiboutik: List Stores

Retrieves stores from Hiboutik.

```
GET https://connect.mindcloud.co/v1/universal/hiboutik/latest/actions/list-stores
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hiboutik `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hiboutik/latest/actions/list-stores?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hiboutik/latest/actions/list-stores?${params}`, {
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
      "discounts": [
        {}
      ],
      "storeDefaultCurrency": "string",
      "storeDefaultPaymentMethod": "string",
      "storeId": 1,
      "storeName": "Ava Chen",
      "storeTimeZone": "string",
      "storeWarehouseId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `discounts` | array<object> |  |
| `storeDefaultCurrency` | string |  |
| `storeDefaultPaymentMethod` | string |  |
| `storeId` | number |  |
| `storeName` | string |  |
| `storeTimeZone` | string |  |
| `storeWarehouseId` | number |  |

## Native endpoint

Through the native Hiboutik API, this operation is `GET /stores` (base URL `https://mindcloudhiboutik20260402.hiboutik.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-stores.md) for the provider-specific parameters and requirements.

