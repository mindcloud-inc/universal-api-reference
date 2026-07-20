# Woztell Universal API Examples

These examples use the MindCloud API key and Woztell connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get App Info

Retrieves app information from your Woztell workspace.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/woztell/latest/actions/get-app-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/woztell/latest/actions/get-app-info?${params}`, {
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
  "data": [],
  "meta": {}
}
```

See the full [Get App Info action reference](actions/get-app-info.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/woztell/latest/actions/get-app-info).

## Create Audience

Creates an audience in your Woztell workspace.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/woztell/latest/actions/create-audience" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/woztell/latest/actions/create-audience', {
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
      "data": {
        "createAudience": {
          "audience": {
            "_id": "string",
            "channelId": "string",
            "createdAt": 1,
            "description": "string",
            "etag": "string",
            "id": "string",
            "name": "Ava Chen",
            "static": true,
            "updatedAt": 1
          },
          "clientMutationId": "string"
        }
      }
    }
  ],
  "meta": {}
}
```

See the full [Create Audience action reference](actions/create-audience.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/woztell/latest/actions/create-audience).
