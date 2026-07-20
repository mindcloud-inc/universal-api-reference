# Dromo Universal API Examples

These examples use the MindCloud API key and Dromo connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Import Schemas

Retrieves all import schemas from Dromo.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dromo/latest/actions/list-import-schemas?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dromo/latest/actions/list-import-schemas?${params}`, {
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

See the full [List Import Schemas action reference](actions/list-import-schemas.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/dromo/latest/actions/list-import-schemas).

## Create Headless Import

Creates a new headless import in Dromo.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dromo/latest/actions/create-headless-import" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dromo/latest/actions/create-headless-import', {
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

See the full [Create Headless Import action reference](actions/create-headless-import.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/dromo/latest/actions/create-headless-import).
