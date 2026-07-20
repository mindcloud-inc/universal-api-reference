# BulkSMS: Update Webhook

Updates an existing webhook in BulkSMS.

```
PUT https://connect.mindcloud.co/v1/universal/bulkSMS/latest/actions/update-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BulkSMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/bulkSMS/latest/actions/update-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "name": "Ava Chen",
  "url": "https://example.com",
  "triggerScope": "0"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bulkSMS/latest/actions/update-webhook', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "name": "Ava Chen",
    "url": "https://example.com",
    "triggerScope": "0"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The webhook ID to update. |
| `name` | string | yes | Webhook name. Names must be unique. |
| `url` | string | yes | Webhook destination URL. Must start with http or https. |
| `triggerScope` | list | yes | Webhook trigger scope: SENT or RECEIVED. One of: `0`, `1`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contactEmailAddress` | string | no | Email address for webhook invocation problem notifications. |
| `invokeOption` | list | no | Whether BulkSMS invokes the webhook with one message or many messages. One of: `0`, `1`. |
| `active` | boolean | no | Whether the webhook should be active after update. |
| `onWebApp` | boolean | no | Whether to show the webhook in the BulkSMS web app. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "contactEmailAddress": "ava@example.com",
      "id": 1,
      "name": "Ava Chen",
      "onWebApp": true,
      "triggerScope": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `contactEmailAddress` | string |  |
| `id` | number |  |
| `name` | string |  |
| `onWebApp` | boolean |  |
| `triggerScope` | string |  |
| `url` | string |  |

## Native endpoint

Through the native BulkSMS API, this operation is `POST /webhooks/:id` (base URL `https://api.bulksms.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-webhook.md) for the provider-specific parameters and requirements.

