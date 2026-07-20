# HelpSpace: Update Webhook

Updates the webhook in HelpSpace.

```
PUT https://connect.mindcloud.co/v1/universal/helpSpace/latest/actions/update-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HelpSpace `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/helpSpace/latest/actions/update-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/helpSpace/latest/actions/update-webhook', {
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
      "enabled": true,
      "failedCount": 1,
      "headers": [
        {}
      ],
      "secret": "string",
      "trigger": {
        "customer": {
          "created": true,
          "deleted": true,
          "updated": true
        },
        "tag": {
          "created": true,
          "deleted": true,
          "updated": true
        },
        "ticket": {
          "agentMessageCreated": true,
          "assigned": true,
          "created": true,
          "customerMessageCreated": true,
          "deleted": true,
          "noteCreated": true,
          "statusUpdated": true,
          "tagsUpdated": true
        }
      },
      "url": "https://example.com",
      "version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `enabled` | boolean |  |
| `failedCount` | number |  |
| `headers` | array<object> |  |
| `secret` | string |  |
| `trigger` | object |  |
| `trigger.customer.created` | boolean |  |
| `trigger.customer.deleted` | boolean |  |
| `trigger.customer.updated` | boolean |  |
| `trigger.tag.created` | boolean |  |
| `trigger.tag.deleted` | boolean |  |
| `trigger.tag.updated` | boolean |  |
| `trigger.ticket.agentMessageCreated` | boolean |  |
| `trigger.ticket.assigned` | boolean |  |
| `trigger.ticket.created` | boolean |  |
| `trigger.ticket.customerMessageCreated` | boolean |  |
| `trigger.ticket.deleted` | boolean |  |
| `trigger.ticket.noteCreated` | boolean |  |
| `trigger.ticket.statusUpdated` | boolean |  |
| `trigger.ticket.tagsUpdated` | boolean |  |
| `url` | string |  |
| `version` | string |  |

## Native endpoint

Through the native HelpSpace API, this operation is `POST /webhook` (base URL `https://api.helpspace.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-webhook.md) for the provider-specific parameters and requirements.

