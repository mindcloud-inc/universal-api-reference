# Deep Infra Universal API Examples

These examples use the MindCloud API key and Deep Infra connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List OpenAI Models



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deepInfra/latest/actions/list-open-ai-models?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/deepInfra/latest/actions/list-open-ai-models?${params}`, {
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
      "created": 1,
      "id": "string",
      "metadata": {
        "contextLength": 1,
        "description": "string",
        "maxTokens": 1,
        "pricing": {
          "cacheReadTokens": 1,
          "inputTokens": 1,
          "outputTokens": 1
        },
        "tags": [
          "string"
        ]
      },
      "object": "string",
      "ownedBy": "Ava Chen",
      "parent": "string",
      "root": "string"
    }
  ],
  "meta": {}
}
```

See the full [List OpenAI Models action reference](actions/list-open-ai-models.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/deepInfra/latest/actions/list-open-ai-models).
