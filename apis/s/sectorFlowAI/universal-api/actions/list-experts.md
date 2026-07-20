# SectorFlow.AI: List Experts



```
GET https://connect.mindcloud.co/v1/universal/sectorFlowAI/latest/actions/list-experts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SectorFlow.AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sectorFlowAI/latest/actions/list-experts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sectorFlowAI/latest/actions/list-experts?${params}`, {
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
| `showPublic` | string | no | Whether to show public expert entries. Defaults to true. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "id": "string",
      "isPublic": true,
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `id` | string |  |
| `isPublic` | boolean |  |
| `title` | string |  |

## Native endpoint

Through the native SectorFlow.AI API, this operation is `GET /plus` (base URL `https://platform.sectorflow.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-experts.md) for the provider-specific parameters and requirements.

