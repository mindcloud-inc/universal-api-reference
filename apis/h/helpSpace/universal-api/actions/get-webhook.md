# HelpSpace: Get Webhook

Retrieves the webhook from HelpSpace.

```
GET https://connect.mindcloud.co/v1/universal/helpSpace/latest/actions/get-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HelpSpace `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/helpSpace/latest/actions/get-webhook?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/helpSpace/latest/actions/get-webhook?${params}`, {
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

Through the native HelpSpace API, this operation is `GET /webhook` (base URL `https://api.helpspace.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-webhook.md) for the provider-specific parameters and requirements.

