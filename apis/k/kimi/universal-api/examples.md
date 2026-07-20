# Kimi Universal API Examples

These examples use the MindCloud API key and Kimi connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Models

Retrieves the available models from Kimi.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kimi/latest/actions/list-models?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kimi/latest/actions/list-models?${params}`, {
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
      "contextLength": 1,
      "created": 1,
      "id": "string",
      "object": "string",
      "ownedBy": "string",
      "parent": "string",
      "permission": [
        {}
      ],
      "root": "string",
      "supportsImageIn": true,
      "supportsReasoning": true,
      "supportsVideoIn": true
    }
  ],
  "meta": {}
}
```

See the full [List Models action reference](actions/list-models.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/kimi/latest/actions/list-models).
