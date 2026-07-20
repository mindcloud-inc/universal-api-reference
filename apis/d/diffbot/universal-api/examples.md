# Diffbot Universal API Examples

These examples use the MindCloud API key and Diffbot connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Account

Retrieves Diffbot account details and usage information.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/diffbot/latest/actions/get-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/diffbot/latest/actions/get-account?${params}`, {
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
      "created": "string",
      "email": "ava@example.com",
      "name": "Ava Chen",
      "plan": "string",
      "planCredits": 1,
      "planStart": "string",
      "status": "string",
      "token": "string",
      "usage": [
        {
          "credits": 1,
          "date": "string",
          "entities": 1,
          "extractions": 1,
          "facets": 1,
          "nlp": 1,
          "proxies": 1,
          "refresh": 1,
          "subtitles": 1,
          "videos": 1
        }
      ]
    }
  ],
  "meta": {}
}
```

See the full [Get Account action reference](actions/get-account.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/diffbot/latest/actions/get-account).
