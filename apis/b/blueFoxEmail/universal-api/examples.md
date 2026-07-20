# BlueFox Email Universal API Examples

These examples use the MindCloud API key and BlueFox Email connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Subscribers

Retrieves subscribers from a BlueFox Email list.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/blueFoxEmail/latest/actions/list-subscribers?connectionId=$CONNECTION_ID&subscriberListId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "subscriberListId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/blueFoxEmail/latest/actions/list-subscribers?${params}`, {
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
      "__v": 1,
      "_id": "string",
      "accountId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "lastReceiveDate": "2026-05-07T12:00:00.000Z",
      "pausedUntil": "2026-05-07T12:00:00.000Z",
      "projectId": "string",
      "status": "string",
      "subscriberListId": "string",
      "tags": [
        "string"
      ],
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [List Subscribers action reference](actions/list-subscribers.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/blueFoxEmail/latest/actions/list-subscribers).

## Activate Subscription

Activates a subscriber in a BlueFox Email list.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/blueFoxEmail/latest/actions/activate-subscription" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "subscriberListId": "string",
  "subscriberEmailAddress": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/blueFoxEmail/latest/actions/activate-subscription', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "subscriberListId": "string",
    "subscriberEmailAddress": "ava@example.com"
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
      "__v": 1,
      "_id": "string",
      "accountId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "lastReceiveDate": "2026-05-07T12:00:00.000Z",
      "pausedUntil": "2026-05-07T12:00:00.000Z",
      "projectId": "string",
      "status": "string",
      "subscriberListId": "string",
      "tags": [
        "string"
      ],
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [Activate Subscription action reference](actions/activate-subscription.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/blueFoxEmail/latest/actions/activate-subscription).
