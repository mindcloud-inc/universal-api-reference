# ActivityInfo Universal API Examples

These examples use the MindCloud API key and ActivityInfo connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Ping ActivityInfo

Checks whether the ActivityInfo API is reachable.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/activityInfo/latest/actions/ping-activity-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/activityInfo/latest/actions/ping-activity-info?${params}`, {
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

See the full [Ping ActivityInfo action reference](actions/ping-activity-info.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/activityInfo/latest/actions/ping-activity-info).
