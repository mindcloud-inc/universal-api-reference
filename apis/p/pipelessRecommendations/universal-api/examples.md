# Pipeless Recommendations Universal API Examples

These examples use the MindCloud API key and Pipeless Recommendations connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Recent Events

Retrieves recent events from Pipeless Recommendations.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pipelessRecommendations/latest/actions/get-recent-events?connectionId=$CONNECTION_ID&appId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "appId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pipelessRecommendations/latest/actions/get-recent-events?${params}`, {
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
      "event": {
        "endObject": {
          "createdOn": "2026-05-07T12:00:00.000Z",
          "id": "string",
          "modifiedOn": "2026-05-07T12:00:00.000Z",
          "type": "string"
        },
        "relationship": {
          "createdOn": "2026-05-07T12:00:00.000Z",
          "type": "string"
        },
        "startObject": {
          "createdOn": "2026-05-07T12:00:00.000Z",
          "id": "string",
          "modifiedOn": "2026-05-07T12:00:00.000Z",
          "type": "string"
        }
      },
      "eventAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [Get Recent Events action reference](actions/get-recent-events.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/pipelessRecommendations/latest/actions/get-recent-events).

## Create Event

Creates a new event in Pipeless Recommendations.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pipelessRecommendations/latest/actions/create-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "appId": "1885"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pipelessRecommendations/latest/actions/create-event', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "appId": "1885"
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
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Create Event action reference](actions/create-event.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/pipelessRecommendations/latest/actions/create-event).
