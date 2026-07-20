# Saleshandy Universal API Examples

These examples use the MindCloud API key and Saleshandy connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Sequences



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/saleshandy/latest/actions/list-sequences?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/saleshandy/latest/actions/list-sequences?${params}`, {
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
      "message": "string",
      "payload": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [List Sequences action reference](actions/list-sequences.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/saleshandy/latest/actions/list-sequences).

## Create Sequence



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/saleshandy/latest/actions/create-sequence" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "title": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/saleshandy/latest/actions/create-sequence', {
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
      "message": "string",
      "payload": {}
    }
  ],
  "meta": {}
}
```

See the full [Create Sequence action reference](actions/create-sequence.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/saleshandy/latest/actions/create-sequence).
