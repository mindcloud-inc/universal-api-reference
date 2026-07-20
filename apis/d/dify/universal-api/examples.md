# Dify Universal API Examples

These examples use the MindCloud API key and Dify connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get App Info

Retrieves application info from Dify.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dify/latest/actions/get-app-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dify/latest/actions/get-app-info?${params}`, {
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
      "authorName": "Ava Chen",
      "description": "string",
      "mode": "string",
      "name": "Ava Chen",
      "tags": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

See the full [Get App Info action reference](actions/get-app-info.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/dify/latest/actions/get-app-info).

## Configure Annotation Reply

Updates annotation reply settings in Dify.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/dify/latest/actions/configure-annotation-reply" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "action": "string",
  "embeddingProviderName": "Ava Chen",
  "embeddingModelName": "Ava Chen",
  "scoreThreshold": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dify/latest/actions/configure-annotation-reply', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "action": "string",
    "embeddingProviderName": "Ava Chen",
    "embeddingModelName": "Ava Chen",
    "scoreThreshold": 1
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
      "jobId": "string",
      "jobStatus": "string"
    }
  ],
  "meta": {}
}
```

See the full [Configure Annotation Reply action reference](actions/configure-annotation-reply.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/dify/latest/actions/configure-annotation-reply).
