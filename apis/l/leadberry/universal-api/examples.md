# Leadberry Universal API Examples

These examples use the MindCloud API key and Leadberry connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Websites



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/leadberry/latest/actions/list-websites?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/leadberry/latest/actions/list-websites?${params}`, {
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

See the full [List Websites action reference](actions/list-websites.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/leadberry/latest/actions/list-websites).

## Add Lead To CRM



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/leadberry/latest/actions/add-lead-to-crm" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/leadberry/latest/actions/add-lead-to-crm', {
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

See the full [Add Lead To CRM action reference](actions/add-lead-to-crm.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/leadberry/latest/actions/add-lead-to-crm).
