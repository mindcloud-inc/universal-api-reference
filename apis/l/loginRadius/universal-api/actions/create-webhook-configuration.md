# LoginRadius: Create Webhook Configuration

Creates a new webhook configuration in LoginRadius.

```
POST https://connect.mindcloud.co/v1/universal/loginRadius/latest/actions/create-webhook-configuration
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LoginRadius `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/loginRadius/latest/actions/create-webhook-configuration" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "event": "VerifyPhoneNumber",
  "name": "Stage3Webhook",
  "targetUrl": "https://httpbin.org/post"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/loginRadius/latest/actions/create-webhook-configuration', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "event": "VerifyPhoneNumber",
    "name": "Stage3Webhook",
    "targetUrl": "https://httpbin.org/post"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `event` | string | yes | Webhook event to subscribe to. Example: `VerifyPhoneNumber`. |
| `name` | string | yes | Webhook configuration name. Example: `Stage3Webhook`. |
| `targetUrl` | string | yes | Webhook destination URL. Example: `https://httpbin.org/post`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "CreatedDate": "2026-05-07T12:00:00.000Z",
      "Event": "string",
      "Id": "string",
      "IsIntegrationWebhook": true,
      "LastModifiedDate": "2026-05-07T12:00:00.000Z",
      "Name": "Ava Chen",
      "TargetUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `CreatedDate` | date | When the webhook was created. |
| `Event` | string | Webhook event type. |
| `Id` | string | Webhook configuration id. |
| `IsIntegrationWebhook` | boolean | Whether the webhook is an integration webhook. |
| `LastModifiedDate` | date | When the webhook was last modified. |
| `Name` | string | Webhook configuration name. |
| `TargetUrl` | string | Webhook destination URL. |

## Native endpoint

Through the native LoginRadius API, this operation is `POST /v2/manage/webhooks` (base URL `https://api.loginradius.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-webhook-configuration.md) for the provider-specific parameters and requirements.

