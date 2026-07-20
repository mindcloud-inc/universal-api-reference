# Dify: List Annotations

Retrieves annotations from Dify.

```
GET https://connect.mindcloud.co/v1/universal/dify/latest/actions/list-annotations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dify/latest/actions/list-annotations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dify/latest/actions/list-annotations?${params}`, {
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
| `page` | number | no | Page number to return. |
| `keyword` | string | no | Keyword filter for annotations. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "answer": "string",
      "createdAt": 1,
      "hitCount": 1,
      "id": "string",
      "question": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `answer` | string |  |
| `createdAt` | number |  |
| `hitCount` | number |  |
| `id` | string |  |
| `question` | string |  |

## Native endpoint

Through the native Dify API, this operation is `GET /apps/annotations` (base URL `https://api.dify.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-annotations.md) for the provider-specific parameters and requirements.

