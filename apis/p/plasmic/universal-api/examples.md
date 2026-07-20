# Plasmic Universal API Examples

These examples use the MindCloud API key and Plasmic connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Count Items

Counts items in Plasmic CMS.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/plasmic/latest/actions/count-items?connectionId=$CONNECTION_ID&modelId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "modelId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/plasmic/latest/actions/count-items?${params}`, {
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
      "count": 1
    }
  ],
  "meta": {}
}
```

See the full [Count Items action reference](actions/count-items.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/plasmic/latest/actions/count-items).

## Create Items

Creates items in Plasmic CMS.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/plasmic/latest/actions/create-items" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "modelId": "string",
  "rows[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/plasmic/latest/actions/create-items', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "modelId": "string",
    "rows[]": [{}]
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
      "rows": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [Create Items action reference](actions/create-items.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/plasmic/latest/actions/create-items).
