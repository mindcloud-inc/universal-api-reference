# Hume AI: Get Prompt



```
GET https://connect.mindcloud.co/v1/universal/humeAI/latest/actions/get-prompt
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hume AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/humeAI/latest/actions/get-prompt?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/humeAI/latest/actions/get-prompt?${params}`, {
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
| `id` | string | yes | Prompt ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "pageNumber": 1,
      "pageSize": 1,
      "promptsPage": [
        {}
      ],
      "totalPages": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `pageNumber` | number | Current page number. |
| `pageSize` | number | Current page size. |
| `promptsPage` | array<object> | Prompts returned for the current page. |
| `totalPages` | number | Total number of pages. |

## Native endpoint

Through the native Hume AI API, this operation is `GET /v0/evi/prompts/:id` (base URL `https://api.hume.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-prompt.md) for the provider-specific parameters and requirements.

