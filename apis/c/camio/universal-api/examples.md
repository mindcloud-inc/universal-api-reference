# Camio Universal API Examples

These examples use the MindCloud API key and Camio connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Connected Cameras

Retrieves connected cameras from Camio.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/camio/latest/actions/list-connected-cameras?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/camio/latest/actions/list-connected-cameras?${params}`, {
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
      "cameraId": "string",
      "capabilities": [
        "string"
      ],
      "isOnline": true,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [List Connected Cameras action reference](actions/list-connected-cameras.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/camio/latest/actions/list-connected-cameras).

## Create Camio

Creates a Camio in Camio.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/camio/latest/actions/create-camio" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "query": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/camio/latest/actions/create-camio', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "query": {}
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
      "creator": {},
      "dateCreated": "string",
      "id": "string",
      "message": {},
      "name": "Ava Chen",
      "owner": {},
      "query": {},
      "type": "string",
      "url": "https://example.com",
      "viewToken": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Camio action reference](actions/create-camio.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/camio/latest/actions/create-camio).
