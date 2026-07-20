# Veryfi: Process a Tls Certificate

Uploads a TLS certificate to Veryfi.

```
POST https://connect.mindcloud.co/v1/universal/veryfi/latest/actions/post-api-v8-partner-settings-tls-certificate
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Veryfi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/veryfi/latest/actions/post-api-v8-partner-settings-tls-certificate" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/veryfi/latest/actions/post-api-v8-partner-settings-tls-certificate', {
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
      "certificate_body": "string",
      "certificate_id": "string",
      "expires_on": "string",
      "id": 1,
      "issued_on": "string",
      "key_body": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `certificate_body` | string |  |
| `certificate_id` | string |  |
| `expires_on` | string |  |
| `id` | number |  |
| `issued_on` | string |  |
| `key_body` | string |  |

## Native endpoint

Through the native Veryfi API, this operation is `POST /api/v8/partner/settings/tls-certificate` (base URL `https://api.veryfi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/post-api-v8-partner-settings-tls-certificate.md) for the provider-specific parameters and requirements.

