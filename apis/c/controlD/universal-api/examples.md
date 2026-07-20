# Control D Universal API Examples

These examples use the MindCloud API key and Control D connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Profiles

Retrieves profiles from Control D.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/controlD/latest/actions/list-profiles?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/controlD/latest/actions/list-profiles?${params}`, {
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
      "name": "Ava Chen",
      "PK": "string",
      "profile": {},
      "stats": 1,
      "updated": 1
    }
  ],
  "meta": {}
}
```

See the full [List Profiles action reference](actions/list-profiles.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/controlD/latest/actions/list-profiles).

## Batch Modify Filters

Updates multiple filters for a profile in Control D.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/controlD/latest/actions/batch-modify-filters" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "profileId": "string",
  "filters[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/controlD/latest/actions/batch-modify-filters', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "profileId": "string",
    "filters[]": [{}]
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
      "value": "string"
    }
  ],
  "meta": {}
}
```

See the full [Batch Modify Filters action reference](actions/batch-modify-filters.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/controlD/latest/actions/batch-modify-filters).
