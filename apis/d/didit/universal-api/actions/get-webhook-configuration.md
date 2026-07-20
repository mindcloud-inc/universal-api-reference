# Didit: Get Webhook Configuration

Retrieves the webhook configuration from Didit.

```
GET https://connect.mindcloud.co/v1/universal/didit/latest/actions/get-webhook-configuration
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Didit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/didit/latest/actions/get-webhook-configuration?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/didit/latest/actions/get-webhook-configuration?${params}`, {
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

Through the native Didit API, this operation is `GET /webhook/` (base URL `https://verification.didit.me/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-webhook-configuration.md) for the provider-specific parameters and requirements.

