# Didit: Update Webhook Configuration

Updates the webhook configuration in Didit.

```
PUT https://connect.mindcloud.co/v1/universal/didit/latest/actions/update-webhook-configuration
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Didit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/didit/latest/actions/update-webhook-configuration" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/didit/latest/actions/update-webhook-configuration', {
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
      "captureMethod": "string",
      "dataRetentionMonths": 1,
      "secretSharedKey": "string",
      "webhookUrl": "https://example.com",
      "webhookVersion": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `captureMethod` | string |  |
| `dataRetentionMonths` | number |  |
| `secretSharedKey` | string |  |
| `webhookUrl` | string |  |
| `webhookVersion` | string |  |

## Native endpoint

Through the native Didit API, this operation is `PATCH /webhook/` (base URL `https://verification.didit.me/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-webhook-configuration.md) for the provider-specific parameters and requirements.

