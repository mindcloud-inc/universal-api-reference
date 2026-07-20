# QuickFile: Get Purchase



```
GET https://connect.mindcloud.co/v1/universal/quickFile/latest/actions/get-purchase
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QuickFile `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quickFile/latest/actions/get-purchase?connectionId=$CONNECTION_ID&purchaseId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "purchaseId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/quickFile/latest/actions/get-purchase?${params}`, {
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
| `purchaseId` | number | yes | Default: `1`. |

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
      "supplierId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `currency` | string |  |
| `invoiceDescription` | string |  |
| `purchaseId` | number |  |
| `receiptDate` | date |  |
| `supplierId` | number |  |

## Native endpoint

Through the native QuickFile API, this operation is `POST /purchase/get` (base URL `https://api.quickfile.co.uk/1_2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-purchase.md) for the provider-specific parameters and requirements.

