# BlackBaud Universal API Examples

These examples use the MindCloud API key and BlackBaud connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Action



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/blackBaud/latest/actions/get-action?connectionId=$CONNECTION_ID&actionId=Action%20ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "actionId": "Action ID"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/blackBaud/latest/actions/get-action?${params}`, {
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

See the full [Get Action action reference](actions/get-action.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/blackBaud/latest/actions/get-action).
