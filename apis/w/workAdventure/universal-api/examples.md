# WorkAdventure Universal API Examples

These examples use the MindCloud API key and WorkAdventure connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Ping map storage

Checks whether WorkAdventure map storage is reachable.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/workAdventure/latest/actions/ping-map-storage?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/workAdventure/latest/actions/ping-map-storage?${params}`, {
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
      "data": [
        1
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [Ping map storage action reference](actions/ping-map-storage.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/workAdventure/latest/actions/ping-map-storage).

## Copy map file

Copies a file in WorkAdventure map storage.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/workAdventure/latest/actions/copy-map-file" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "source": "string",
  "destination": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/workAdventure/latest/actions/copy-map-file', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "source": "string",
    "destination": "string"
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
      "data": [
        1
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [Copy map file action reference](actions/copy-map-file.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/workAdventure/latest/actions/copy-map-file).
