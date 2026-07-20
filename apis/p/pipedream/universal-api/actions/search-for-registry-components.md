# Pipedream: Search for registry components

Finds registry components in Pipedream by natural-language query.

```
GET https://connect.mindcloud.co/v1/universal/pipedream/latest/actions/search-for-registry-components
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pipedream `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pipedream/latest/actions/search-for-registry-components?connectionId=$CONNECTION_ID&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pipedream/latest/actions/search-for-registry-components?${params}`, {
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
| `appSlug` | string | no | Optional app name slug to filter results for a single app. |
| `debug` | boolean | no | Return additional debug data for result inspection when true. |
| `query` | string | yes | The natural-language query used to search the global registry. |
| `similarityThreshold` | number | no | Optional minimum similarity score between 0 and 1. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "actions": [
        "string"
      ],
      "sources": [
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
| `actions` | array<string> |  |
| `sources` | array<string> |  |

## Native endpoint

Through the native Pipedream API, this operation is `GET /components/search` (base URL `https://api.pipedream.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-for-registry-components.md) for the provider-specific parameters and requirements.

