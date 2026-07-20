# Invidious: Get Search Suggestions



```
GET https://connect.mindcloud.co/v1/universal/invidious/latest/actions/get-search-suggestions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Invidious `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/invidious/latest/actions/get-search-suggestions?connectionId=$CONNECTION_ID&query=ambient%20music" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "ambient music"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/invidious/latest/actions/get-search-suggestions?${params}`, {
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
| `query` | string | yes | Search text for suggestions. Example: `ambient music`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "query": "string",
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
| `query` | string |  |
| `suggestions` | array<string> |  |

## Native endpoint

Through the native Invidious API, this operation is `GET /search/suggestions` (base URL `{{credentials.instanceUrl}}/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-search-suggestions.md) for the provider-specific parameters and requirements.

