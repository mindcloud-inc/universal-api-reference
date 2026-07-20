# Ringg AI: Get Assistants

Retrieves assistants from Ringg AI.

```
GET https://connect.mindcloud.co/v1/universal/ringgAI/latest/actions/get-assistants
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ringg AI `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ringgAI/latest/actions/get-assistants?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ringgAI/latest/actions/get-assistants?${params}`, {
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
      "data": {
        "agents": [
          {
            "agentDisplayName": "Ava Chen",
            "agentType": "string",
            "callCount": 1,
            "createdAt": "2026-05-07T12:00:00.000Z",
            "customVariables": {},
            "id": "string",
            "isArchived": true,
            "secondaryLanguage": "string",
            "secondaryVoiceId": "string",
            "templateIcon": "string",
            "templateLabel": "string",
            "templateName": "Ava Chen",
            "templateSource": "string",
            "templateType": "string",
            "tools": [
              {}
            ],
            "updatedAt": "2026-05-07T12:00:00.000Z"
          }
        ]
      },
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `data.agents` | array<object> |  |
| `data.agents[].agentDisplayName` | string |  |
| `data.agents[].agentType` | string |  |
| `data.agents[].callCount` | number |  |
| `data.agents[].createdAt` | date |  |
| `data.agents[].customVariables` | object |  |
| `data.agents[].id` | string |  |
| `data.agents[].isArchived` | boolean |  |
| `data.agents[].secondaryLanguage` | string |  |
| `data.agents[].secondaryVoiceId` | string |  |
| `data.agents[].templateIcon` | string |  |
| `data.agents[].templateLabel` | string |  |
| `data.agents[].templateName` | string |  |
| `data.agents[].templateSource` | string |  |
| `data.agents[].templateType` | string |  |
| `data.agents[].tools` | array<object> |  |
| `data.agents[].updatedAt` | date |  |
| `status` | string |  |

## Native endpoint

Through the native Ringg AI API, this operation is `GET /agent/all` (base URL `https://prod-api.ringg.ai/ca/api/v0`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-assistants.md) for the provider-specific parameters and requirements.

