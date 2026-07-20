# Basin Universal API Examples

These examples use the MindCloud API key and Basin connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Domains

Retrieves domain records from Basin.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/basin/latest/actions/list-domains?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/basin/latest/actions/list-domains?${params}`, {
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

See the full [List Domains action reference](actions/list-domains.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/basin/latest/actions/list-domains).

## Create Form

Creates a new form in Basin.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/basin/latest/actions/create-form" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "form.name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/basin/latest/actions/create-form', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "form.name": "Ava Chen"
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

See the full [Create Form action reference](actions/create-form.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/basin/latest/actions/create-form).
