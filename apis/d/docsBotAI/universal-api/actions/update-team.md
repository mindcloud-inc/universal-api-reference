# DocsBot AI: Update Team

Updates an existing team in DocsBot AI.

```
PUT https://connect.mindcloud.co/v1/universal/docsBotAI/latest/actions/update-team
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DocsBot AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/docsBotAI/latest/actions/update-team" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "teamId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/docsBotAI/latest/actions/update-team', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "teamId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `teamId` | string | yes | The DocsBot team ID. |

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

Through the native DocsBot AI API, this operation is `PUT /teams/:teamId` (base URL `https://docsbot.ai/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-team.md) for the provider-specific parameters and requirements.

