# Robots for Power BI Universal API Examples

These examples use the MindCloud API key and Robots for Power BI connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Disable playlist

Disables a playlist in Robots for Power BI.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/robotsForPowerBI/latest/actions/disable-playlist" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "00000000-0000-0000-0000-000000000000"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/robotsForPowerBI/latest/actions/disable-playlist', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "00000000-0000-0000-0000-000000000000"
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
      "error": "string",
      "message": "string",
      "ok": true,
      "playlist": {
        "cronDescription": "string",
        "cronExpression": "string",
        "id": "string",
        "title": "string"
      }
    }
  ],
  "meta": {}
}
```

See the full [Disable playlist action reference](actions/disable-playlist.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/robotsForPowerBI/latest/actions/disable-playlist).
