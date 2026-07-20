# PushAlert Universal API Examples

These examples use the MindCloud API key and PushAlert connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get All Segments



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pushAlert/latest/actions/get-all-segments?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pushAlert/latest/actions/get-all-segments?${params}`, {
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
      "segments": [
        {}
      ],
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Get All Segments action reference](actions/get-all-segments.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/pushAlert/latest/actions/get-all-segments).

## Add Subscriber Attributes



```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/pushAlert/latest/actions/add-subscriber-attributes" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "subscriber": "string",
  "attributes": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pushAlert/latest/actions/add-subscriber-attributes', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "subscriber": "string",
    "attributes": "string"
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
      "msg": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Add Subscriber Attributes action reference](actions/add-subscriber-attributes.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/pushAlert/latest/actions/add-subscriber-attributes).
