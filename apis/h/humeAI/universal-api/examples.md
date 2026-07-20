# Hume AI Universal API Examples

These examples use the MindCloud API key and Hume AI connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Configs

Retrieves EVI configs from Hume AI.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/humeAI/latest/actions/list-configs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/humeAI/latest/actions/list-configs?${params}`, {
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
      "configsPage": [
        {}
      ],
      "pageNumber": 1,
      "pageSize": 1,
      "totalPages": 1
    }
  ],
  "meta": {}
}
```

See the full [List Configs action reference](actions/list-configs.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/humeAI/latest/actions/list-configs).

## Convert Voice File

Converts uploaded audio in Hume AI and returns a streamed audio file.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/humeAI/latest/actions/convert-voice-file" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "audio": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/humeAI/latest/actions/convert-voice-file', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "audio": "string"
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
      "data": [
        1
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [Convert Voice File action reference](actions/convert-voice-file.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/humeAI/latest/actions/convert-voice-file).
