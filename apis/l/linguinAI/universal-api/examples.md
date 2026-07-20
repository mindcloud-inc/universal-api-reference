# Linguin AI Universal API Examples

These examples use the MindCloud API key and Linguin AI connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Account Status



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/linguinAI/latest/actions/get-account-status?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/linguinAI/latest/actions/get-account-status?${params}`, {
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
      "daily_limit": 1,
      "detections_today": 1,
      "remaining_today": 1
    }
  ],
  "meta": {}
}
```

See the full [Get Account Status action reference](actions/get-account-status.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/linguinAI/latest/actions/get-account-status).

## Bulk Detect Language



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/linguinAI/latest/actions/bulk-detect-language" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "q[]": "Enter one text per item"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/linguinAI/latest/actions/bulk-detect-language', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "q[]": "Enter one text per item"
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "results": [
        [
          "string"
        ]
      ]
    }
  ],
  "meta": {}
}
```

See the full [Bulk Detect Language action reference](actions/bulk-detect-language.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/linguinAI/latest/actions/bulk-detect-language).
