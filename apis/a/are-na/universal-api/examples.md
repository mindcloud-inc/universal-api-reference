# Are.na Universal API Examples

These examples use the MindCloud API key and Are.na connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current User

Retrieves the current user from Are.na.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/are-na/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/are-na/latest/actions/get-current-user?${params}`, {
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
      "_links": {},
      "avatar": {},
      "counts": {},
      "id": 1,
      "name": "Ava Chen",
      "slug": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Current User action reference](actions/get-current-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/are-na/latest/actions/get-current-user).

## Create Block

Creates a new block in Are.na.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/are-na/latest/actions/create-block" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "channel_ids[]": [
    1
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/are-na/latest/actions/create-block', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "channel_ids[]": [1]
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
      "_links": {},
      "content": {},
      "id": 1,
      "source": {},
      "title": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Block action reference](actions/create-block.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/are-na/latest/actions/create-block).
