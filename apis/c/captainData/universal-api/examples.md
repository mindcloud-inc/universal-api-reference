# Captain Data Universal API Examples

These examples use the MindCloud API key and Captain Data connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Quotas

Retrieves workspace quota details from Captain Data.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/captainData/latest/actions/get-quotas?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/captainData/latest/actions/get-quotas?${params}`, {
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
      "credits_max": 1,
      "credits_used": 1,
      "current_month_end": "string",
      "current_month_start": "string",
      "name": "Ava Chen",
      "plan_name": "Ava Chen",
      "uid": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Quotas action reference](actions/get-quotas.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/captainData/latest/actions/get-quotas).
