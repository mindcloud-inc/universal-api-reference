# ManyChat Universal API Examples

These examples use the MindCloud API key and ManyChat connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Page Info

Retrieves connected page details from ManyChat.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/manyChat/latest/actions/get-page-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/manyChat/latest/actions/get-page-info?${params}`, {
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
      "about": {},
      "avatarLink": {},
      "category": {},
      "description": {},
      "id": {},
      "isPro": true,
      "name": "Ava Chen",
      "timezone": "string",
      "username": {}
    }
  ],
  "meta": {}
}
```

See the full [Get Page Info action reference](actions/get-page-info.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/manyChat/latest/actions/get-page-info).

## Add Tag To Subscriber

Adds a tag to a subscriber in ManyChat.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/manyChat/latest/actions/add-tag-to-subscriber" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "subscriber_id": 1,
  "tag_id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/manyChat/latest/actions/add-tag-to-subscriber', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "subscriber_id": 1,
    "tag_id": 1
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
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add Tag To Subscriber action reference](actions/add-tag-to-subscriber.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/manyChat/latest/actions/add-tag-to-subscriber).
