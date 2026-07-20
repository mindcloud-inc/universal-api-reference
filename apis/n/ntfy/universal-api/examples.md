# ntfy Universal API Examples

These examples use the MindCloud API key and ntfy connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Cached Topic Messages

Retrieves cached messages from an ntfy topic.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ntfy/latest/actions/list-cached-topic-messages?connectionId=$CONNECTION_ID&topic=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "topic": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ntfy/latest/actions/list-cached-topic-messages?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "actions": [
        {}
      ],
      "attachment": {},
      "click": "string",
      "event": "string",
      "expires": 1,
      "id": "string",
      "message": "string",
      "priority": 1,
      "sequence_id": "string",
      "tags": [
        "string"
      ],
      "time": 1,
      "title": "string",
      "topic": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Cached Topic Messages action reference](actions/list-cached-topic-messages.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/ntfy/latest/actions/list-cached-topic-messages).

## Publish Alertmanager Template Notification

Publishes an ntfy notification from the Alertmanager template.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/ntfy/latest/actions/publish-alertmanager-template-notification" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ntfy/latest/actions/publish-alertmanager-template-notification', {
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

Example response:

```json
{
  "success": true,
  "data": [
    {
      "actions": [
        {}
      ],
      "attachment": {},
      "click": "string",
      "event": "string",
      "expires": 1,
      "id": "string",
      "message": "string",
      "priority": 1,
      "sequence_id": "string",
      "tags": [
        "string"
      ],
      "time": 1,
      "title": "string",
      "topic": "string"
    }
  ],
  "meta": {}
}
```

See the full [Publish Alertmanager Template Notification action reference](actions/publish-alertmanager-template-notification.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/ntfy/latest/actions/publish-alertmanager-template-notification).
