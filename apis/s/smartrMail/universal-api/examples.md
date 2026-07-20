# SmartrMail Universal API Examples

These examples use the MindCloud API key and SmartrMail connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Subscriber Lists

Retrieves subscriber lists from your SmartrMail account.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smartrMail/latest/actions/list-subscriber-lists?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smartrMail/latest/actions/list-subscriber-lists?${params}`, {
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
      "id": "string",
      "name": "Ava Chen",
      "subscribers_count": 1
    }
  ],
  "meta": {}
}
```

See the full [List Subscriber Lists action reference](actions/list-subscriber-lists.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/smartrMail/latest/actions/list-subscriber-lists).

## Add Subscribers to List

Adds subscribers to a specific SmartrMail list.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/smartrMail/latest/actions/add-subscribers-to-list" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "listId": "string",
  "subscribers": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/smartrMail/latest/actions/add-subscribers-to-list', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "listId": "string",
    "subscribers": {}
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
      "clicked_count": 1,
      "complained": true,
      "custom_fields": [
        {}
      ],
      "delivered_count": 1,
      "email": "ava@example.com",
      "first_name": "Ava",
      "id": "string",
      "joined_at": "2026-05-07T12:00:00.000Z",
      "last_name": "Chen",
      "opened_count": 1,
      "phone": "string",
      "subscribed": true,
      "unsubscribed_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [Add Subscribers to List action reference](actions/add-subscribers-to-list.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/smartrMail/latest/actions/add-subscribers-to-list).
