# Look Digital Signage Universal API Examples

These examples use the MindCloud API key and Look Digital Signage connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Trigger Action

Triggers a configured action in Look Digital Signage.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/lookDigitalSignage/latest/actions/trigger-action" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "actionLink": "https://...your-look-action-link..."
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lookDigitalSignage/latest/actions/trigger-action', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "actionLink": "https://...your-look-action-link..."
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

See the full [Trigger Action action reference](actions/trigger-action.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/lookDigitalSignage/latest/actions/trigger-action).
