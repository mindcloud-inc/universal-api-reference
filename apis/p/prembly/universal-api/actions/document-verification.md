# Prembly: Document Verification

Creates a document verification in Prembly.

```
POST https://connect.mindcloud.co/v1/universal/prembly/latest/actions/document-verification
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Prembly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/prembly/latest/actions/document-verification" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/prembly/latest/actions/document-verification', {
  method: 'POST',
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
      "age": 1,
      "device": {
        "HasContactlessChipReader": true,
        "HasMagneticStripeReader": true,
        "SerialNumber": "string",
        "Type": {
          "Manufacturer": "string",
          "Model": "string",
          "SensorType": 1
        }
      },
      "dob": "2026-05-07T12:00:00.000Z",
      "document_name": "Ava Chen",
      "documentCountry": "string",
      "documentNumber": "string",
      "documentType": "string",
      "expirationDate": "2026-05-07T12:00:00.000Z",
      "fullName": "Ava Chen",
      "gender": "string",
      "issuer": "string",
      "status": {
        "description": "string",
        "match_status": true
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `age` | number |  |
| `device.HasContactlessChipReader` | boolean |  |
| `device.HasMagneticStripeReader` | boolean |  |
| `device.SerialNumber` | string |  |
| `device.Type.Manufacturer` | string |  |
| `device.Type.Model` | string |  |
| `device.Type.SensorType` | number |  |
| `dob` | date |  |
| `document_name` | string |  |
| `documentCountry` | string |  |
| `documentNumber` | string |  |
| `documentType` | string |  |
| `expirationDate` | date |  |
| `fullName` | string |  |
| `gender` | string |  |
| `issuer` | string |  |
| `status.description` | string |  |
| `status.match_status` | boolean |  |

## Native endpoint

Through the native Prembly API, this operation is `POST /verification/document` (base URL `https://api.prembly.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/document-verification.md) for the provider-specific parameters and requirements.

