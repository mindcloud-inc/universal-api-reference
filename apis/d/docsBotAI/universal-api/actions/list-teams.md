# DocsBot AI: List Teams

Retrieves teams from DocsBot AI.

```
GET https://connect.mindcloud.co/v1/universal/docsBotAI/latest/actions/list-teams
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DocsBot AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docsBotAI/latest/actions/list-teams?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/docsBotAI/latest/actions/list-teams?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "botCount": 1,
      "chunkCount": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "name": "Ava Chen",
      "openAIKey": "string",
      "pageCount": 1,
      "plan": {},
      "questionCount": 1,
      "roles": {},
      "sourceCount": 1,
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `botCount` | number |  |
| `chunkCount` | number |  |
| `createdAt` | date |  |
| `id` | string |  |
| `name` | string |  |
| `openAIKey` | string |  |
| `pageCount` | number |  |
| `plan` | object |  |
| `questionCount` | number |  |
| `roles` | object |  |
| `sourceCount` | number |  |
| `status` | string |  |

## Native endpoint

Through the native DocsBot AI API, this operation is `GET /teams` (base URL `https://docsbot.ai/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-teams.md) for the provider-specific parameters and requirements.

