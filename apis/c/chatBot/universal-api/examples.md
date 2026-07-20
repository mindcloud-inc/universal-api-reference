# ChatBot Universal API Examples

These examples use the MindCloud API key and ChatBot connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Stories

Retrieves chatbot story records from ChatBot API.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chatBot/latest/actions/list-stories?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chatBot/latest/actions/list-stories?${params}`, {
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
      "description": "string",
      "id": "string",
      "metrics": [
        {}
      ],
      "name": "Ava Chen",
      "published": true,
      "version": 1
    }
  ],
  "meta": {}
}
```

See the full [List Stories action reference](actions/list-stories.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/chatBot/latest/actions/list-stories).

## Add segments to User

Adds segments to an existing ChatBot user.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/chatBot/latest/actions/add-segments-to-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "69baf2590ee62a000879d09c",
  "segmentIds[]": "69baf25884fd9e0007485fcf"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chatBot/latest/actions/add-segments-to-user', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "69baf2590ee62a000879d09c",
    "segmentIds[]": "69baf25884fd9e0007485fcf"
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
      "status": {},
      "timestamp": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [Add segments to User action reference](actions/add-segments-to-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/chatBot/latest/actions/add-segments-to-user).
