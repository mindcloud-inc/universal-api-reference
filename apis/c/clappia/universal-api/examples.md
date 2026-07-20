# Clappia Universal API Examples

These examples use the MindCloud API key and Clappia connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Workplace Users

Retrieves workplace users from your Clappia workplace.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clappia/latest/actions/list-workplace-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clappia/latest/actions/list-workplace-users?${params}`, {
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
      "canCreateApps": "string",
      "emailAddress": "ava@example.com",
      "name": "Ava Chen",
      "phoneNumber": "string",
      "role": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Workplace Users action reference](actions/list-workplace-users.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/clappia/latest/actions/list-workplace-users).

## Add Chart

Creates a new chart in Clappia.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/clappia/latest/actions/add-chart" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "appId": "string",
  "chartIndex": 1,
  "chartType": "string",
  "aggregationDimensions[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clappia/latest/actions/add-chart', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "appId": "string",
    "chartIndex": 1,
    "chartType": "string",
    "aggregationDimensions[]": [{}]
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [],
  "meta": {}
}
```

See the full [Add Chart action reference](actions/add-chart.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/clappia/latest/actions/add-chart).
