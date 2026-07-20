# Salesforge: Create Webhook

Creates a webhook in Salesforge.

```
POST https://connect.mindcloud.co/v1/universal/salesforge/latest/actions/create-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Salesforge `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/salesforge/latest/actions/create-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workspaceId": "wks_lxxtq91neaixc8yaiqp7w",
  "name": "Stage 3 Reply Webhook",
  "type": "email_replied",
  "url": "https://example.com/salesforge-stage3-webhook"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/salesforge/latest/actions/create-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workspaceId": "wks_lxxtq91neaixc8yaiqp7w",
    "name": "Stage 3 Reply Webhook",
    "type": "email_replied",
    "url": "https://example.com/salesforge-stage3-webhook"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `workspaceId` | string | yes | Example: `wks_lxxtq91neaixc8yaiqp7w`. |
| `name` | string | yes | Example: `Stage 3 Reply Webhook`. |
| `type` | list | yes | One of: `contact_unsubscribed`, `dnc_added`, `email_bounced`, `email_opened`, `email_replied`, `email_sent`, `label_changed`, `link_clicked`, `linkedin_replied`, `negative_reply`, `positive_reply`. Example: `email_replied`. |
| `url` | string | yes | Example: `https://example.com/salesforge-stage3-webhook`. |
| `sequenceId` | string | no | Example: `seq_123`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "name": "Ava Chen",
      "sentCount": 1,
      "type": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `name` | string |  |
| `sentCount` | number |  |
| `type` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Salesforge API, this operation is `POST /public/v2/workspaces/:workspaceID/integrations/webhooks` (base URL `https://api.salesforge.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-webhook.md) for the provider-specific parameters and requirements.

