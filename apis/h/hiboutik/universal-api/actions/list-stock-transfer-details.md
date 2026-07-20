# Hiboutik: List Stock Transfer Details

Retrieves stock transfer details from Hiboutik.

```
GET https://connect.mindcloud.co/v1/universal/hiboutik/latest/actions/list-stock-transfer-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hiboutik `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hiboutik/latest/actions/list-stock-transfer-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hiboutik/latest/actions/list-stock-transfer-details?${params}`, {
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
      "productId": 1,
      "quantity": "string",
      "transferId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `productId` | number |  |
| `quantity` | string |  |
| `transferId` | number |  |

## Native endpoint

Through the native Hiboutik API, this operation is `GET /stock_transfer_details/:transfer_id` (base URL `https://mindcloudhiboutik20260402.hiboutik.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-stock-transfer-details.md) for the provider-specific parameters and requirements.

