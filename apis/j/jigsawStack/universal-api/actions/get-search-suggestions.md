# JigsawStack: Get Search Suggestions



```
GET https://connect.mindcloud.co/v1/universal/jigsawStack/latest/actions/get-search-suggestions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a JigsawStack `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jigsawStack/latest/actions/get-search-suggestions?connectionId=$CONNECTION_ID&query=What%20is%20the%20capital" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "What is the capital"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jigsawStack/latest/actions/get-search-suggestions?${params}`, {
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
| `query` | string | yes | The partial search phrase to autocomplete. Example: `What is the capital`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_usage": {},
      "log_id": "string",
      "success": true,
      "suggestions": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_usage` | object |  |
| `log_id` | string |  |
| `success` | boolean |  |
| `suggestions` | array<string> |  |

## Native endpoint

Through the native JigsawStack API, this operation is `GET /v1/web/search/suggest` (base URL `https://api.jigsawstack.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-search-suggestions.md) for the provider-specific parameters and requirements.

