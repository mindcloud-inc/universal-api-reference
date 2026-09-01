# Amark: Get Receipt Info



```
GET https://connect.mindcloud.co/v1/universal/amarkAWL/latest/actions/get-receipt-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Amark `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/amarkAWL/latest/actions/get-receipt-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/amarkAWL/latest/actions/get-receipt-info?${params}`, {
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
      "context": "string",
      "event": "string",
      "status": 1,
      "successData": {
        "arrivalDate": "string",
        "dateCreated": "string",
        "dateUpdated": "string",
        "id": 1,
        "items": [
          {
            "code": "string",
            "description": "string",
            "quantity": 1,
            "remainingQuantity": 1
          }
        ],
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
| `successData.dateCreated` | string |  |
| `successData.dateUpdated` | string |  |
| `successData.id` | number |  |
| `successData.items[].code` | string |  |
| `successData.items[].description` | string |  |
| `successData.items[].quantity` | number |  |
| `successData.items[].remainingQuantity` | number |  |
| `successData.referenceNumber` | string |  |
| `successData.remoteNotes` | string |  |
| `successData.supplierId` | number |  |
| `successData.trackingNumber` | string |  |

## Native endpoint

Through the native Amark API, this operation is `POST /Receipt/Info` (base URL `{{credentials.environment}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-receipt-info.md) for the provider-specific parameters and requirements.

