# e-Boekhouden.nl Universal API Examples

These examples use the MindCloud API key and e-Boekhouden.nl connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Relations

Retrieves relations from e-Boekhouden.nl.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/e-boekhouden-nl/latest/actions/list-relations?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/e-boekhouden-nl/latest/actions/list-relations?${params}`, {
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

See the full [List Relations action reference](actions/list-relations.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/e-boekhouden-nl/latest/actions/list-relations).

## Create Cost Center

Creates a new cost center in e-Boekhouden.nl.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/e-boekhouden-nl/latest/actions/create-cost-center" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/e-boekhouden-nl/latest/actions/create-cost-center', {
  method: 'POST',
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
  "data": [],
  "meta": {}
}
```

See the full [Create Cost Center action reference](actions/create-cost-center.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/e-boekhouden-nl/latest/actions/create-cost-center).
