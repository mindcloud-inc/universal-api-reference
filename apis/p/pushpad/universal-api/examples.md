# Pushpad Universal API Examples

These examples use the MindCloud API key and Pushpad connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Projects

Retrieves all projects available in Pushpad.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pushpad/latest/actions/list-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pushpad/latest/actions/list-projects?${params}`, {
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
      "badgeUrl": "https://example.com",
      "createdAt": "string",
      "iconUrl": "https://example.com",
      "id": 1,
      "name": "Ava Chen",
      "notificationsRequireInteraction": true,
      "notificationsSilent": true,
      "notificationsTtl": 1,
      "senderId": 1,
      "url": "https://example.com",
      "website": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Projects action reference](actions/list-projects.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/pushpad/latest/actions/list-projects).

## Create or Import Subscription

Creates or imports a subscription into a Pushpad project.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pushpad/latest/actions/create-or-import-subscription" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "endpoint": "string",
  "projectId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pushpad/latest/actions/create-or-import-subscription', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "endpoint": "string",
    "projectId": 1
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
      "auth": "string",
      "createdAt": "string",
      "endpoint": "string",
      "id": 1,
      "lastClickAt": "string",
      "p256dh": "string",
      "projectId": 1,
      "tags": [
        "string"
      ],
      "uid": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create or Import Subscription action reference](actions/create-or-import-subscription.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/pushpad/latest/actions/create-or-import-subscription).
