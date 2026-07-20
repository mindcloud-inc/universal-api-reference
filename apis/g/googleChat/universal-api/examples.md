# Google Chat Universal API Examples

These examples use the MindCloud API key and Google Chat connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Spaces

Retrieves Google Chat spaces the caller is a member of.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleChat/latest/actions/list-spaces?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleChat/latest/actions/list-spaces?${params}`, {
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
      "createTime": "2026-05-07T12:00:00.000Z",
      "customer": "string",
      "displayName": "Ava Chen",
      "lastActiveTime": "2026-05-07T12:00:00.000Z",
      "membershipCount": {},
      "name": "Ava Chen",
      "spaceHistoryState": "string",
      "spaceThreadingState": "string",
      "spaceType": "string",
      "spaceUri": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Spaces action reference](actions/list-spaces.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/googleChat/latest/actions/list-spaces).

## Create Message

Creates a message in a Google Chat space.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/googleChat/latest/actions/create-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "space": "4Oe1TyAAAAE",
  "text": "Hello from MindCloud"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/googleChat/latest/actions/create-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "space": "4Oe1TyAAAAE",
    "text": "Hello from MindCloud"
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [],
  "meta": {}
}
```

See the full [Create Message action reference](actions/create-message.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/googleChat/latest/actions/create-message).
