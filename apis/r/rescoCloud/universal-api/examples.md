# Resco Cloud Universal API Examples

These examples use the MindCloud API key and Resco Cloud connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Who Am I

Retrieves the current organization and user IDs from Resco Cloud.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rescoCloud/latest/actions/who-am-i?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rescoCloud/latest/actions/who-am-i?${params}`, {
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

See the full [Who Am I action reference](actions/who-am-i.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/rescoCloud/latest/actions/who-am-i).

## Create Multiple Records

Creates multiple records in Resco Cloud.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rescoCloud/latest/actions/create-multiple-records" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "rawBody": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rescoCloud/latest/actions/create-multiple-records', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "rawBody": "string"
  })
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

See the full [Create Multiple Records action reference](actions/create-multiple-records.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/rescoCloud/latest/actions/create-multiple-records).
