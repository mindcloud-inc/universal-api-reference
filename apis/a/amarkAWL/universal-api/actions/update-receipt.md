# Amark: Update Receipt



```
PUT https://connect.mindcloud.co/v1/universal/amarkAWL/latest/actions/update-receipt
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Amark `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/amarkAWL/latest/actions/update-receipt" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/amarkAWL/latest/actions/update-receipt', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "context": "string",
      "event": "string",
      "status": 1,
      "successData": {
        "arrivalDate": "string",
        "id": 1,
        "modifyItems": [
          {
            "productId": 1,
            "quantity": 1
          }
        ],
        "receiptModifyId": 1,
        "referenceNumber": "string",
        "remoteNotes": "string",
        "supplierId": 1,
        "trackingNumber": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `context` | string |  |
| `event` | string |  |
| `status` | number |  |
| `successData.arrivalDate` | string |  |
| `successData.id` | number |  |
| `successData.modifyItems[].productId` | number |  |
| `successData.modifyItems[].quantity` | number |  |
| `successData.receiptModifyId` | number |  |
| `successData.referenceNumber` | string |  |
| `successData.remoteNotes` | string |  |
| `successData.supplierId` | number |  |
| `successData.trackingNumber` | string |  |

## Native endpoint

Through the native Amark API, this operation is `POST /Receipt/Modify` (base URL `{{credentials.environment}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-receipt.md) for the provider-specific parameters and requirements.

