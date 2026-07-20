# DocsBot AI: List Questions

Retrieves questions from DocsBot AI.

```
GET https://connect.mindcloud.co/v1/universal/docsBotAI/latest/actions/list-questions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DocsBot AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docsBotAI/latest/actions/list-questions?connectionId=$CONNECTION_ID&botId=string&teamId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "botId": "string",
  "teamId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/docsBotAI/latest/actions/list-questions?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `botId` | string | yes | The DocsBot bot ID. |
| `teamId` | string | yes | The DocsBot team ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "pagination": {},
      "questions": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `pagination` | object |  |
| `questions` | array<object> |  |

## Native endpoint

Through the native DocsBot AI API, this operation is `GET /teams/:teamId/bots/:botId/questions` (base URL `https://docsbot.ai/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-questions.md) for the provider-specific parameters and requirements.

