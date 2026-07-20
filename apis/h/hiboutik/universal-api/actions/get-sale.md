# Hiboutik: Get Sale

Retrieves a sale from Hiboutik.

```
GET https://connect.mindcloud.co/v1/universal/hiboutik/latest/actions/get-sale
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hiboutik `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hiboutik/latest/actions/get-sale?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hiboutik/latest/actions/get-sale?${params}`, {
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
      "customersId": 1,
      "details": [
        {}
      ],
      "saleId": 1,
      "total": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `customersId` | number |  |
| `details` | array<object> |  |
| `saleId` | number |  |
| `total` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Hiboutik API, this operation is `GET /sales/:sale_id` (base URL `https://mindcloudhiboutik20260402.hiboutik.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-sale.md) for the provider-specific parameters and requirements.

