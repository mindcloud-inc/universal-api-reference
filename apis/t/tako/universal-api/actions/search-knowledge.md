# Tako: Search Knowledge

Searches Tako Knowledge Cards with natural language.

```
GET https://connect.mindcloud.co/v1/universal/tako/latest/actions/search-knowledge
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tako `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tako/latest/actions/search-knowledge?connectionId=$CONNECTION_ID&inputs.text=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "inputs.text": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tako/latest/actions/search-knowledge?${params}`, {
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
| `inputs.searchEffort` | string | no | Optional search depth. Provider docs describe `fast`, `deep`, and `auto` modes. |
| `inputs.text` | string | yes | Natural-language query text to send to Tako. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "outputs": {},
      "request_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `outputs` | object | Search output payload containing returned knowledge cards and optional answer text. |
| `request_id` | string | Unique request identifier returned by Tako. |

## Native endpoint

Through the native Tako API, this operation is `POST /v1/knowledge_search` (base URL `https://tako.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-knowledge.md) for the provider-specific parameters and requirements.

