# Storyscale Universal API Examples

These examples use the MindCloud API key and Storyscale connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Search Experiences, Sequences, and Assets



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/storyscale/latest/actions/search-experiences-sequences-and-assets?connectionId=$CONNECTION_ID&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/storyscale/latest/actions/search-experiences-sequences-and-assets?${params}`, {
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
      "data": {},
      "status": {}
    }
  ],
  "meta": {}
}
```

See the full [Search Experiences, Sequences, and Assets action reference](actions/search-experiences-sequences-and-assets.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/storyscale/latest/actions/search-experiences-sequences-and-assets).

## Add Assets To Sequences



```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/storyscale/latest/actions/add-assets-to-sequences" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/storyscale/latest/actions/add-assets-to-sequences', {
  method: 'PUT',
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
      "data": {},
      "status": {}
    }
  ],
  "meta": {}
}
```

See the full [Add Assets To Sequences action reference](actions/add-assets-to-sequences.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/storyscale/latest/actions/add-assets-to-sequences).
