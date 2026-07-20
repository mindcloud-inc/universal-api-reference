# MessageBird: List Conversation Participants



```
GET https://connect.mindcloud.co/v1/universal/messageBird/latest/actions/list-conversation-participants
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MessageBird `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/messageBird/latest/actions/list-conversation-participants?connectionId=$CONNECTION_ID&workspaceId=string&conversationId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspaceId": "string",
  "conversationId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/messageBird/latest/actions/list-conversation-participants?${params}`, {
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
| `workspaceId` | string | yes | The Bird workspace ID that owns the conversation. |
| `conversationId` | string | yes | The Bird conversation ID whose participants should be listed. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "nextPageToken": "string",
      "results": [
        {}
      ],
      "total": 1,
      "totalType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `nextPageToken` | string | The token that can be passed as pageToken in URL to retrieve the next set of results. If missing, no more results to display. |
| `results` | array<object> | List of conversation participants. |
| `total` | number |  |
| `totalType` | string |  |

## Native endpoint

Through the native MessageBird API, this operation is `GET /workspaces/:workspaceId/conversations/:conversationId/participants` (base URL `https://api.bird.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-conversation-participants.md) for the provider-specific parameters and requirements.

