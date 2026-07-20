# Fairing Universal API Examples

These examples use the MindCloud API key and Fairing connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Questions

Retrieves questions from Fairing.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fairing/latest/actions/list-questions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fairing/latest/actions/list-questions?${params}`, {
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
      "allowOther": true,
      "customerType": "string",
      "frequencyType": "string",
      "id": 1,
      "insertedAt": "2026-05-07T12:00:00.000Z",
      "otherPlaceholder": "string",
      "prompt": "string",
      "publishedAt": "2026-05-07T12:00:00.000Z",
      "randomizeResponses": true,
      "responses": [
        {}
      ],
      "submitText": "string",
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [List Questions action reference](actions/list-questions.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/fairing/latest/actions/list-questions).
