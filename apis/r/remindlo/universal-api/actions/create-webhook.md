# Remindlo: Create Webhook



```
POST https://connect.mindcloud.co/v1/universal/remindlo/latest/actions/create-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Remindlo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/remindlo/latest/actions/create-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "eventTypes[]": [
    "string"
  ],
  "name": "Ava Chen",
  "targetUrl": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/remindlo/latest/actions/create-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "eventTypes[]": ["string"],
    "name": "Ava Chen",
    "targetUrl": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `eventTypes[]` | array<string> | yes |  |
| `name` | string | yes |  |
| `targetUrl` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "endpoint": {},
      "signing_secret": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `endpoint` | object | Created webhook endpoint details. |
| `signing_secret` | string | Webhook signing secret returned once at creation time. |
| `success` | boolean | Whether the webhook endpoint was created successfully. |

## Native endpoint

Through the native Remindlo API, this operation is `POST /webhooks` (base URL `https://api.remindlo.co.uk/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-webhook.md) for the provider-specific parameters and requirements.

