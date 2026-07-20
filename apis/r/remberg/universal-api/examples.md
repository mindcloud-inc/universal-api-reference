# remberg Universal API Examples

These examples use the MindCloud API key and remberg connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Assets

Retrieves assets from remberg.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/remberg/latest/actions/list-assets?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/remberg/latest/actions/list-assets?${params}`, {
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

See the full [List Assets action reference](actions/list-assets.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/remberg/latest/actions/list-assets).

## Approve Work Request By External Reference

Approves a work request in remberg by external reference.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/remberg/latest/actions/approve-work-request-by-external-reference" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/remberg/latest/actions/approve-work-request-by-external-reference', {
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
  "data": [],
  "meta": {}
}
```

See the full [Approve Work Request By External Reference action reference](actions/approve-work-request-by-external-reference.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/remberg/latest/actions/approve-work-request-by-external-reference).
