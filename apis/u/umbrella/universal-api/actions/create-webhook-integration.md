# Umbrella: Create Webhook Integration

Creates a new webhook integration in Umbrella.

```
POST https://connect.mindcloud.co/v1/universal/umbrella/latest/actions/create-webhook-integration
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Umbrella `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/umbrella/latest/actions/create-webhook-integration" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/umbrella/latest/actions/create-webhook-integration', {
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

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | no | The integration name. |
| `type` | string | no | The integration type. |
| `webhookConfig.url` | string | no | The destination URL for webhook integrations. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "href": "https://example.com",
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `href` | string |  |
| `id` | string |  |

## Native endpoint

Through the native Umbrella API, this operation is `POST https://api.sse.cisco.com/admin/v2/integrations` (base URL `https://api.umbrella.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-webhook-integration.md) for the provider-specific parameters and requirements.

