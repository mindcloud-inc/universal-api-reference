# Roborabbit Universal API Examples

These examples use the MindCloud API key and Roborabbit connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Account

Retrieves account status and quota usage from Roborabbit.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/roborabbit/latest/actions/get-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/roborabbit/latest/actions/get-account?${params}`, {
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
      "apiQuota": 1,
      "apiUsage": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "plan": "string",
      "uid": "string",
      "workspace": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Account action reference](actions/get-account.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/roborabbit/latest/actions/get-account).

## Create Run

Creates a new run for a Roborabbit task.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/roborabbit/latest/actions/create-run" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "taskUid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/roborabbit/latest/actions/create-run', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "taskUid": "string"
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
      "createdAt": "2026-05-07T12:00:00.000Z",
      "finishedInSeconds": 1,
      "metadata": "string",
      "outputs": [
        "string"
      ],
      "status": "string",
      "steps": [
        {}
      ],
      "task": "string",
      "uid": "string",
      "videoUrl": "https://example.com",
      "webhookUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Create Run action reference](actions/create-run.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/roborabbit/latest/actions/create-run).
