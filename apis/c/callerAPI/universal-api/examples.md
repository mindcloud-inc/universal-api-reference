# CallerAPI Universal API Examples

These examples use the MindCloud API key and CallerAPI connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Balance and Email

Retrieves account balance and email from CallerAPI.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/callerAPI/latest/actions/get-balance-and-email?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/callerAPI/latest/actions/get-balance-and-email?${params}`, {
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
      "credits_left": 1,
      "credits_monthly": 1,
      "credits_spent": 1,
      "email": "ava@example.com",
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Balance and Email action reference](actions/get-balance-and-email.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/callerAPI/latest/actions/get-balance-and-email).
