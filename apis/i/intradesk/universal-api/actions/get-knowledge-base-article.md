# Intradesk: Get Knowledge Base Article

Retrieves a knowledge base article from Intradesk.

```
GET https://connect.mindcloud.co/v1/universal/intradesk/latest/actions/get-knowledge-base-article
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Intradesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/intradesk/latest/actions/get-knowledge-base-article?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/intradesk/latest/actions/get-knowledge-base-article?${params}`, {
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
| `id` | string | yes | Knowledge base article identifier from Intradesk Knowledgebase API path. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdat": "2026-05-07T12:00:00.000Z",
      "createdby": "string",
      "createdid": 1,
      "description": "string",
      "files": "string",
      "id": 1,
      "name": "Ava Chen",
      "servicepath": [
        {}
      ],
      "services": [
        {}
      ],
      "updatedat": "2026-05-07T12:00:00.000Z",
      "updatedby": "string",
      "updatedid": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdat` | date |  |
| `createdby` | string |  |
| `createdid` | number |  |
| `description` | string |  |
| `files` | string |  |
| `id` | number |  |
| `name` | string |  |
| `servicepath` | array<object> |  |
| `services` | array<object> |  |
| `updatedat` | date |  |
| `updatedby` | string |  |
| `updatedid` | number |  |

## Native endpoint

Through the native Intradesk API, this operation is `GET /knowledgebase/api/v1/Kb/{id}` (base URL `https://apigw.intradesk.ru`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-knowledge-base-article.md) for the provider-specific parameters and requirements.

