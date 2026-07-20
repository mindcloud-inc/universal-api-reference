# Prembly: Tax Identification Number Check

Creates a tax identification number check in Prembly.

```
POST https://connect.mindcloud.co/v1/universal/prembly/latest/actions/tax-identification-number-check
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Prembly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/prembly/latest/actions/tax-identification-number-check" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/prembly/latest/actions/tax-identification-number-check', {
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
      "data": "string",
      "detail": "string",
      "endpoint_name": "Ava Chen",
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
| `data` | string |  |
| `detail` | string |  |
| `endpoint_name` | string |  |
| `response_code` | string |  |
| `status` | boolean |  |
| `verification.reference` | string |  |
| `verification.status` | string |  |

## Native endpoint

Through the native Prembly API, this operation is `POST /verification/global/tin-check` (base URL `https://api.prembly.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/tax-identification-number-check.md) for the provider-specific parameters and requirements.

