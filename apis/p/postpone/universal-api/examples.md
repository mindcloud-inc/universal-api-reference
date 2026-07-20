# Postpone Universal API Examples

These examples use the MindCloud API key and Postpone connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Aggregate Post Metrics

Retrieves aggregate post metrics from Postpone.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/postpone/latest/actions/get-aggregate-post-metrics?connectionId=$CONNECTION_ID&variables.startDate=string&variables.endDate=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "variables.startDate": "string",
  "variables.endDate": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/postpone/latest/actions/get-aggregate-post-metrics?${params}`, {
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
      "metrics": [
        {
          "aggregation": "string",
          "metric": "string",
          "value": 1
        }
      ]
    }
  ],
  "meta": {}
}
```

See the full [Get Aggregate Post Metrics action reference](actions/get-aggregate-post-metrics.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/postpone/latest/actions/get-aggregate-post-metrics).

## Schedule Bluesky Post

Schedules a Bluesky post in Postpone.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/postpone/latest/actions/schedule-bluesky-post" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "variables.input.username": "Ava Chen",
  "variables.input.postAt": "string",
  "variables.input.thread[].text": "string",
  "variables.input.thread[].order": 1,
  "variables.input.thread[].contentWarning": "NONE"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/postpone/latest/actions/schedule-bluesky-post', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "variables.input.username": "Ava Chen",
    "variables.input.postAt": "string",
    "variables.input.thread[].text": "string",
    "variables.input.thread[].order": 1,
    "variables.input.thread[].contentWarning": "NONE"
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
      "scheduleBlueskyPost": {
        "errors": [
          {
            "field": "string",
            "message": "string"
          }
        ],
        "post": {
          "id": "string"
        },
        "success": true
      }
    }
  ],
  "meta": {}
}
```

See the full [Schedule Bluesky Post action reference](actions/schedule-bluesky-post.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/postpone/latest/actions/schedule-bluesky-post).
