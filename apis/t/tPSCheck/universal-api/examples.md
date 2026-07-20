# TPSCheck Universal API Examples

These examples use the MindCloud API key and TPSCheck connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get credits



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tPSCheck/latest/actions/get-credits?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tPSCheck/latest/actions/get-credits?${params}`, {
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
      "monthlyLimit": 1,
      "plan": "string",
      "requestsRemaining": 1,
      "requestsUsed": 1,
      "resetDate": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [Get credits action reference](actions/get-credits.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/tPSCheck/latest/actions/get-credits).
