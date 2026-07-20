# Prembly: Document Verification with Face

Creates document verification with face in Prembly.

```
POST https://connect.mindcloud.co/v1/universal/prembly/latest/actions/document-verification-with-face
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Prembly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/prembly/latest/actions/document-verification-with-face" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/prembly/latest/actions/document-verification-with-face', {
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
      "address": "string",
      "age": "string",
      "date_of_issue": "string",
      "dob": "2026-05-07T12:00:00.000Z",
      "document_name": "Ava Chen",
      "documentCountry": "string",
      "documentNumber": "string",
      "documentType": "string",
      "expirationDate": "2026-05-07T12:00:00.000Z",
      "first_name": "Ava",
      "fullName": "Ava Chen",
      "gender": "string",
      "image": "string",
      "issuer": "string",
      "last_name": "Chen",
      "nationality": "string",
      "place_of_issue": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string |  |
| `age` | string |  |
| `date_of_issue` | string |  |
| `dob` | date |  |
| `document_name` | string |  |
| `documentCountry` | string |  |
| `documentNumber` | string |  |
| `documentType` | string |  |
| `expirationDate` | date |  |
| `first_name` | string |  |
| `fullName` | string |  |
| `gender` | string |  |
| `image` | string |  |
| `issuer` | string |  |
| `last_name` | string |  |
| `nationality` | string |  |
| `place_of_issue` | string |  |

## Native endpoint

Through the native Prembly API, this operation is `POST /verification/document_w_face` (base URL `https://api.prembly.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/document-verification-with-face.md) for the provider-specific parameters and requirements.

