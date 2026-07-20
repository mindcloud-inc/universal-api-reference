# CallTrackingMetrics Universal API Examples

These examples use the MindCloud API key and CallTrackingMetrics connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Active Account IDs And Names

Retrieves active account IDs and names from CallTrackingMetrics.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/callTrackingMetrics/latest/actions/list-active-account-ids-and-names?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/callTrackingMetrics/latest/actions/list-active-account-ids-and-names?${params}`, {
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
      "accounts": [
        [
          {}
        ]
      ]
    }
  ],
  "meta": {}
}
```

See the full [List Active Account IDs And Names action reference](actions/list-active-account-ids-and-names.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/callTrackingMetrics/latest/actions/list-active-account-ids-and-names).

## Create Tracking Source

Creates a new tracking source in CallTrackingMetrics.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/callTrackingMetrics/latest/actions/create-tracking-source" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/callTrackingMetrics/latest/actions/create-tracking-source', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
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
      "source": {
        "accountId": 1,
        "defaultCost": "string",
        "description": "string",
        "id": "string",
        "name": "Ava Chen",
        "online": true,
        "position": 1
      },
      "url": "https://example.com",
      "warnings": {}
    }
  ],
  "meta": {}
}
```

See the full [Create Tracking Source action reference](actions/create-tracking-source.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/callTrackingMetrics/latest/actions/create-tracking-source).
