# Renderly Universal API Examples

These examples use the MindCloud API key and Renderly connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Verify API Key

Verifies an API key in Renderly.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/renderly/latest/actions/verify-api-key?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/renderly/latest/actions/verify-api-key?${params}`, {
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
      "apiKeyCreatedAt": "2026-05-07T12:00:00.000Z",
      "apiKeyLastUsed": "2026-05-07T12:00:00.000Z",
      "apiKeyPrefix": "string",
      "credits": 1,
      "email": "ava@example.com",
      "name": "Ava Chen",
      "userId": "string"
    }
  ],
  "meta": {}
}
```

See the full [Verify API Key action reference](actions/verify-api-key.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/renderly/latest/actions/verify-api-key).

## Create Render Job

Creates a video render job in Renderly.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/renderly/latest/actions/create-render-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/renderly/latest/actions/create-render-job', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
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
      "creditsUsed": 1,
      "estimatedDurationMinutes": 1,
      "jobId": "string",
      "mode": "string",
      "projectId": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Render Job action reference](actions/create-render-job.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/renderly/latest/actions/create-render-job).
