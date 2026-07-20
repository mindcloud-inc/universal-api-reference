# Port API AI: Search Entities

Finds entities in Port.

```
GET https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/search-entities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Port API AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/search-entities?connectionId=$CONNECTION_ID&combinator=string&rules%5B%5D=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "combinator": "string",
  "rules[]": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/search-entities?${params}`, {
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
| `combinator` | string | yes | Search combinator |
| `rules[]` | array<object> | yes | Search rules |

## Response

```json
{
  "success": true,
  "data": [
    {
      "entities": [
        {}
      ],
      "failedBlueprints": [
        "string"
      ],
      "matchingBlueprints": [
        "string"
      ],
      "ok": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `entities` | array<object> |  |
| `failedBlueprints` | array<string> |  |
| `matchingBlueprints` | array<string> |  |
| `ok` | boolean |  |

## Native endpoint

Through the native Port API AI API, this operation is `POST /entities/search` (base URL `https://api.port.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-entities.md) for the provider-specific parameters and requirements.

