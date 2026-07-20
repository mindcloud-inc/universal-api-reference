# Interzoid Universal API Examples

These examples use the MindCloud API key and Interzoid connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Remaining Credits



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/interzoid/latest/actions/get-remaining-credits?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/interzoid/latest/actions/get-remaining-credits?${params}`, {
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
      "Code": "string",
      "Credits": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Remaining Credits action reference](actions/get-remaining-credits.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/interzoid/latest/actions/get-remaining-credits).
