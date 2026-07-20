# Klenty: Add Webhook

Creates a webhook in Klenty.

```
POST https://connect.mindcloud.co/v1/universal/klenty/latest/actions/add-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Klenty `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/klenty/latest/actions/add-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "subscriptionUrl": "https://example.com",
  "event": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/klenty/latest/actions/add-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "subscriptionUrl": "https://example.com",
    "event": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `subscriptionUrl` | string | yes | Webhook destination URL. |
| `event` | string | yes | Webhook event name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "event": "string",
      "Id": "string",
      "isSecured": true,
      "newWebhook": true,
      "token": {},
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `event` | string |  |
| `Id` | string |  |
| `isSecured` | boolean |  |
| `newWebhook` | boolean |  |
| `token` | object |  |
| `url` | string |  |

## Native endpoint

Through the native Klenty API, this operation is `POST /zapier/hooks` (base URL `https://api.klenty.com/apis/v1/user/{{credentials.username}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-webhook.md) for the provider-specific parameters and requirements.

