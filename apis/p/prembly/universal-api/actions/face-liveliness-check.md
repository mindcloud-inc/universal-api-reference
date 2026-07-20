# Prembly: Face Liveliness Check

Creates a face liveliness check in Prembly.

```
POST https://connect.mindcloud.co/v1/universal/prembly/latest/actions/face-liveliness-check
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Prembly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/prembly/latest/actions/face-liveliness-check" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/prembly/latest/actions/face-liveliness-check', {
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
      "confidence": 1,
      "confidence_in_percentage": 1,
      "detail": "string",
      "response_code": "string",
      "status": true,
      "verification": {
        "reference": "string",
        "status": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `confidence` | number |  |
| `confidence_in_percentage` | number |  |
| `detail` | string |  |
| `response_code` | string |  |
| `status` | boolean |  |
| `verification.reference` | string |  |
| `verification.status` | string |  |

## Native endpoint

Through the native Prembly API, this operation is `POST /verification/biometrics/face/liveliness_check` (base URL `https://api.prembly.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/face-liveliness-check.md) for the provider-specific parameters and requirements.

