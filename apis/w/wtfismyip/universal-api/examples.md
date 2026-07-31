# wtfismyip Universal API Examples

These examples use the MindCloud API key and wtfismyip connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Runner IP as Text



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wtfismyip/latest/actions/get-runner-ip-as-text?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wtfismyip/latest/actions/get-runner-ip-as-text?${params}`, {
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

See the full [Get Runner IP as Text action reference](actions/get-runner-ip-as-text.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/wtfismyip/latest/actions/get-runner-ip-as-text).
