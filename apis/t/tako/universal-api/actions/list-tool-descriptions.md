# Tako: List Tool Descriptions

Retrieves tool descriptions from Tako.

```
GET https://connect.mindcloud.co/v1/universal/tako/latest/actions/list-tool-descriptions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tako `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tako/latest/actions/list-tool-descriptions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tako/latest/actions/list-tool-descriptions?${params}`, {
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
| `indexIds` | string | no | Optional comma-separated index IDs to scope the returned tool descriptions. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "search_tools": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `search_tools` | array<object> | List of Tako search tool descriptors. |

## Native endpoint

Through the native Tako API, this operation is `GET /v1/tako_tools_description` (base URL `https://tako.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-tool-descriptions.md) for the provider-specific parameters and requirements.

