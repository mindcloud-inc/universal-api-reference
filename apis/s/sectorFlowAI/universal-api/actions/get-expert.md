# SectorFlow.AI: Get Expert



```
GET https://connect.mindcloud.co/v1/universal/sectorFlowAI/latest/actions/get-expert
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SectorFlow.AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sectorFlowAI/latest/actions/get-expert?connectionId=$CONNECTION_ID&plusId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "plusId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sectorFlowAI/latest/actions/get-expert?${params}`, {
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
| `plusId` | string | yes | The expert UUID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "context": "string",
      "created": "string",
      "description": "string",
      "files": [
        {}
      ],
      "id": "string",
      "isPublic": true,
      "title": "string",
      "userId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `context` | string |  |
| `created` | string |  |
| `description` | string |  |
| `files` | array<object> |  |
| `id` | string |  |
| `isPublic` | boolean |  |
| `title` | string |  |
| `userId` | number |  |

## Native endpoint

Through the native SectorFlow.AI API, this operation is `GET /plus/{plusId}` (base URL `https://platform.sectorflow.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-expert.md) for the provider-specific parameters and requirements.

