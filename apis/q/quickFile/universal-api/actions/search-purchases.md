# QuickFile: Search Purchases



```
GET https://connect.mindcloud.co/v1/universal/quickFile/latest/actions/search-purchases
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QuickFile `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quickFile/latest/actions/search-purchases?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/quickFile/latest/actions/search-purchases?${params}`, {
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
      "currency": "string",
      "invoiceDescription": "string",
      "purchaseId": 1,
      "receiptDate": "2026-05-07T12:00:00.000Z",
      "supplierId": 1,
      "totalAmount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `currency` | string | Purchase currency. |
| `invoiceDescription` | string | Purchase invoice description. |
| `purchaseId` | number | QuickFile purchase identifier. |
| `receiptDate` | date | Purchase receipt date. |
| `supplierId` | number | Supplier identifier linked to the purchase. |
| `totalAmount` | number | Purchase gross total. |

## Native endpoint

Through the native QuickFile API, this operation is `POST /purchase/search` (base URL `https://api.quickfile.co.uk/1_2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-purchases.md) for the provider-specific parameters and requirements.

