# Foreplay Universal API Examples

These examples use the MindCloud API key and Foreplay connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Usage

Retrieves your Foreplay account usage details.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/foreplay/latest/actions/get-usage?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/foreplay/latest/actions/get-usage?${params}`, {
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
      "end_date": "2026-05-07T12:00:00.000Z",
      "remaining_credits": 1,
      "start_date": "2026-05-07T12:00:00.000Z",
      "total_credits": 1,
      "user": {
        "email": "ava@example.com",
        "id": "string"
      }
    }
  ],
  "meta": {}
}
```

See the full [Get Usage action reference](actions/get-usage.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/foreplay/latest/actions/get-usage).
