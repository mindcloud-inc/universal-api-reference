# Toast Universal API Examples

These examples use the MindCloud API key and Toast connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Dining Option

Retrieves one dining option by Toast GUID.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/toast/latest/actions/get-dining-option?connectionId=$CONNECTION_ID&guid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "guid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/toast/latest/actions/get-dining-option?${params}`, {
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

See the full [Get Dining Option action reference](actions/get-dining-option.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/toast/latest/actions/get-dining-option).
