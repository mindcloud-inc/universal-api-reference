# Mona AI: Get Company Knowledge

Retrieves company knowledge from Mona AI.

```
GET https://connect.mindcloud.co/v1/universal/monaAI/latest/actions/get-company-knowledge
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mona AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/monaAI/latest/actions/get-company-knowledge?connectionId=$CONNECTION_ID&permission=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "permission": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/monaAI/latest/actions/get-company-knowledge?${params}`, {
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
| `category` | string | no | Knowledge category to retrieve. |
| `limit` | number | no | Maximum knowledge records to return. |
| `offset` | number | no | Offset for knowledge records. |
| `permission` | string | yes | Mona permission string required by the knowledge endpoint. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Mona AI API returns.

## Native endpoint

Through the native Mona AI API, this operation is `POST /companyKnowledge/getKnowledge` (base URL `https://api.mona-ai.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-company-knowledge.md) for the provider-specific parameters and requirements.

