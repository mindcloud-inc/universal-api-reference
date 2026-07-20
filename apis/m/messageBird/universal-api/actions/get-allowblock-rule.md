# MessageBird: Get Allow/Block Rule



```
GET https://connect.mindcloud.co/v1/universal/messageBird/latest/actions/get-allowblock-rule
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MessageBird `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/messageBird/latest/actions/get-allowblock-rule?connectionId=$CONNECTION_ID&workspaceId=string&allowBlockRuleId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspaceId": "string",
  "allowBlockRuleId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/messageBird/latest/actions/get-allowblock-rule?${params}`, {
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
| `workspaceId` | string | yes | The Bird workspace ID that owns the allow/block rule. |
| `allowBlockRuleId` | string | yes | The Bird allow/block rule ID to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "category": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdBy": "string",
      "id": "string",
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "updatedBy": "string",
      "value": "string",
      "workspaceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `category` | string | The category of the AllowBlockRule. |
| `createdAt` | date |  |
| `createdBy` | string |  |
| `id` | string |  |
| `type` | string | The type of the AllowBlockRule. |
| `updatedAt` | date |  |
| `updatedBy` | string |  |
| `value` | string |  |
| `workspaceId` | string |  |

## Native endpoint

Through the native MessageBird API, this operation is `GET /workspaces/:workspaceId/conversation-allowblock-rules/:allowBlockRuleId` (base URL `https://api.bird.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-allowblock-rule.md) for the provider-specific parameters and requirements.

