# Acronis Universal API Examples

These examples use the MindCloud API key and Acronis connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Tenants

Retrieves a list of tenants from Acronis.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/acronis/latest/actions/list-tenants?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/acronis/latest/actions/list-tenants?${params}`, {
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

See the full [List Tenants action reference](actions/list-tenants.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/acronis/latest/actions/list-tenants).

## Apply Protection Plan To Resources

Applies a protection plan to resources in Acronis.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/acronis/latest/actions/apply-protection-plan-to-resources" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/acronis/latest/actions/apply-protection-plan-to-resources', {
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

See the full [Apply Protection Plan To Resources action reference](actions/apply-protection-plan-to-resources.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/acronis/latest/actions/apply-protection-plan-to-resources).
