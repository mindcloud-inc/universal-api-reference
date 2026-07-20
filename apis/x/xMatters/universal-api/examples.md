# xMatters Universal API Examples

These examples use the MindCloud API key and xMatters connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get People

Retrieves people from your xMatters instance.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-people?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-people?${params}`, {
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
      "count": 1,
      "data": [
        {
          "externallyOwned": true,
          "firstName": "Ava",
          "id": "string",
          "language": "string",
          "lastLogin": "2026-05-07T12:00:00.000Z",
          "lastName": "Chen",
          "links": {
            "self": "https://example.com"
          },
          "recipientType": "string",
          "site": {
            "id": "string",
            "links": {
              "self": "https://example.com"
            }
          },
          "status": "string",
          "targetName": "Ava Chen",
          "timezone": "string",
          "webLogin": "string"
        }
      ],
      "links": {
        "next": "https://example.com",
        "self": "https://example.com"
      },
      "total": 1
    }
  ],
  "meta": {}
}
```

See the full [Get People action reference](actions/get-people.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/xMatters/latest/actions/get-people).

## Add a comment to an event

Adds a comment to an event in your xMatters instance.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/add-a-comment-to-an-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/add-a-comment-to-an-event', {
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
      "author": {
        "firstName": "Ava",
        "id": "string",
        "lastName": "Chen",
        "links": {
          "self": "https://example.com"
        },
        "recipientType": "string",
        "targetName": "Ava Chen"
      },
      "comment": "string",
      "created": "2026-05-07T12:00:00.000Z",
      "event": {
        "eventId": "string",
        "id": "string",
        "links": {
          "self": "https://example.com"
        }
      },
      "id": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add a comment to an event action reference](actions/add-a-comment-to-an-event.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/xMatters/latest/actions/add-a-comment-to-an-event).
