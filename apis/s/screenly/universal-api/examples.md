# Screenly Universal API Examples

These examples use the MindCloud API key and Screenly connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Groups

Retrieves groups from Screenly.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/screenly/latest/actions/list-groups?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/screenly/latest/actions/list-groups?${params}`, {
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
      "screens": [
        {
          "coords": [
            1
          ],
          "id": "string",
          "name": "Ava Chen"
        }
      ],
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [List Groups action reference](actions/list-groups.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/screenly/latest/actions/list-groups).

## Create Asset

Creates a new asset in Screenly.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/screenly/latest/actions/create-asset" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "sourceUrl": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/screenly/latest/actions/create-asset', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "sourceUrl": "https://example.com"
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
      "assetUrl": "https://example.com",
      "disableVerification": true,
      "duration": 1,
      "finalized": true,
      "height": 1,
      "id": "string",
      "md5": "string",
      "metadata": {},
      "sourceMd5": "string",
      "sourceUrl": "https://example.com",
      "status": "string",
      "title": "string",
      "type": "string",
      "url": "https://example.com",
      "width": 1
    }
  ],
  "meta": {}
}
```

See the full [Create Asset action reference](actions/create-asset.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/screenly/latest/actions/create-asset).
