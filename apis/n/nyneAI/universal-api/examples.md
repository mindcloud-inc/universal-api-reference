# Nyne AI Universal API Examples

These examples use the MindCloud API key and Nyne AI connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get API Usage

Retrieves API usage details from Nyne AI.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nyneAI/latest/actions/get-api-usage?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nyneAI/latest/actions/get-api-usage?${params}`, {
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
      "breakdown": {},
      "credits_by_api": {},
      "limits": {},
      "month": 1,
      "period": "string",
      "success": true,
      "timestamp": "2026-05-07T12:00:00.000Z",
      "year": 1
    }
  ],
  "meta": {}
}
```

See the full [Get API Usage action reference](actions/get-api-usage.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/nyneAI/latest/actions/get-api-usage).
