# ZeroBounce Universal API Examples

These examples use the MindCloud API key and ZeroBounce connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Credit Balance

Retrieves credit balance details from ZeroBounce.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zeroBounce/latest/actions/get-credit-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zeroBounce/latest/actions/get-credit-balance?${params}`, {
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
      "credits": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Credit Balance action reference](actions/get-credit-balance.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/zeroBounce/latest/actions/get-credit-balance).
