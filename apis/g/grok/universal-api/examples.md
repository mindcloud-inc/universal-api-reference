# Grok Universal API Examples

These examples use the MindCloud API key and Grok connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get API Key

Retrieves the authenticated API key from Grok.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/grok/latest/actions/get-api-key?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/grok/latest/actions/get-api-key?${params}`, {
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
      "acls": [
        "string"
      ],
      "apiKeyBlocked": true,
      "apiKeyDisabled": true,
      "apiKeyId": "string",
      "createTime": "string",
      "modifiedBy": "string",
      "modifyTime": "string",
      "name": "Ava Chen",
      "redactedApiKey": "string",
      "teamBlocked": true,
      "teamId": "string",
      "userId": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get API Key action reference](actions/get-api-key.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/grok/latest/actions/get-api-key).

## Add Batch Requests to Batch

Creates batch requests in a Grok batch.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/grok/latest/actions/add-batch-requests-to-batch" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "batchId": "string",
  "batchRequests[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/grok/latest/actions/add-batch-requests-to-batch', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "batchId": "string",
    "batchRequests[]": [{}]
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

See the full [Add Batch Requests to Batch action reference](actions/add-batch-requests-to-batch.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/grok/latest/actions/add-batch-requests-to-batch).
