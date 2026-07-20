# SectorFlow.AI: Get Paged Prompt Logs



```
GET https://connect.mindcloud.co/v1/universal/sectorFlowAI/latest/actions/get-paged-prompt-logs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SectorFlow.AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sectorFlowAI/latest/actions/get-paged-prompt-logs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sectorFlowAI/latest/actions/get-paged-prompt-logs?${params}`, {
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
| `pageable` | string | no | Pagination information required by the API. |
| `q` | string | no | Optional prompt log search query. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "content": [
        {}
      ],
      "empty": true,
      "first": true,
      "last": true,
      "number": 1,
      "numberOfElements": 1,
      "pageable": {},
      "size": 1,
      "sort": {},
      "totalElements": 1,
      "totalPages": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content` | array<object> |  |
| `empty` | boolean |  |
| `first` | boolean |  |
| `last` | boolean |  |
| `number` | number |  |
| `numberOfElements` | number |  |
| `pageable` | object |  |
| `size` | number |  |
| `sort` | object |  |
| `totalElements` | number |  |
| `totalPages` | number |  |

## Native endpoint

Through the native SectorFlow.AI API, this operation is `GET /chat/prompt-logs/paged` (base URL `https://platform.sectorflow.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-paged-prompt-logs.md) for the provider-specific parameters and requirements.

