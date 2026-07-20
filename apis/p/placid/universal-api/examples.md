# Placid Universal API Examples

These examples use the MindCloud API key and Placid connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Templates

Finds templates in Placid by collection, title, or tag.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/placid/latest/actions/list-templates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/placid/latest/actions/list-templates?${params}`, {
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
      "collections": [
        "string"
      ],
      "customData": "string",
      "height": 1,
      "layers": [
        {}
      ],
      "tags": [
        "string"
      ],
      "thumbnail": "string",
      "title": "string",
      "uuid": "string",
      "width": 1
    }
  ],
  "meta": {}
}
```

See the full [List Templates action reference](actions/list-templates.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/placid/latest/actions/list-templates).

## Create Collection

Creates a new collection in Placid.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/placid/latest/actions/create-collection" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "title": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/placid/latest/actions/create-collection', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "title": "string"
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
      "customData": "string",
      "id": "string",
      "templates": [
        "string"
      ],
      "title": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Collection action reference](actions/create-collection.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/placid/latest/actions/create-collection).
