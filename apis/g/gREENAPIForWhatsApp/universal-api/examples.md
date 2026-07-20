# GREEN-API for WhatsApp Universal API Examples

These examples use the MindCloud API key and GREEN-API for WhatsApp connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Instance State

Retrieves the WhatsApp instance state from GREEN-API.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gREENAPIForWhatsApp/latest/actions/get-instance-state?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gREENAPIForWhatsApp/latest/actions/get-instance-state?${params}`, {
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
  "data": [
    {
      "stateInstance": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Instance State action reference](actions/get-instance-state.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/gREENAPIForWhatsApp/latest/actions/get-instance-state).
