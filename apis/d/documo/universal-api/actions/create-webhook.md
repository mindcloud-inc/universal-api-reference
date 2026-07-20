# Documo: Create Webhook

Creates a new webhook in Documo.

```
POST https://connect.mindcloud.co/v1/universal/documo/latest/actions/create-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Documo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/documo/latest/actions/create-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/documo/latest/actions/create-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "url": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Webhook name. |
| `url` | string | yes | Webhook URL. |
| `events` | string | no | Webhook events payload. |
| `auth` | string | no | Basic auth in username:password format. |
| `accountId` | string | no | Account UUID. |
| `numberId` | string | no | Fax number UUID. |
| `notificationEmails` | string | no | Notification email recipients. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": "string",
      "attachmentEnabled": true,
      "authType": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "enabled": true,
      "name": "Ava Chen",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | string |  |
| `attachmentEnabled` | boolean |  |
| `authType` | string |  |
| `createdAt` | date |  |
| `enabled` | boolean |  |
| `name` | string |  |
| `updatedAt` | date |  |
| `url` | string |  |
| `uuid` | string |  |

## Native endpoint

Through the native Documo API, this operation is `POST /webhooks` (base URL `https://api.documo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-webhook.md) for the provider-specific parameters and requirements.

