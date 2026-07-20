# SeaX: List API Keys

Retrieves API keys from the current SeaX workspace.

```
GET https://connect.mindcloud.co/v1/universal/seaX/latest/actions/list-api-keys
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SeaX `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/seaX/latest/actions/list-api-keys?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/seaX/latest/actions/list-api-keys?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {}
      ],
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> | API keys returned by the workspace. |
| `total` | number | Total number of API keys. |

## Native endpoint

Through the native SeaX API, this operation is `GET /api_keys` (base URL `https://seax.seasalt.ai/seax-api/api/v1/workspace/{{credentials.workspaceId}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-api-keys.md) for the provider-specific parameters and requirements.

