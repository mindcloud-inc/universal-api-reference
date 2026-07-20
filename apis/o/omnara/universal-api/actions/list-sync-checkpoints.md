# Omnara: List Sync Checkpoints



```
GET https://connect.mindcloud.co/v1/universal/omnara/latest/actions/list-sync-checkpoints
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Omnara `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/omnara/latest/actions/list-sync-checkpoints?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/omnara/latest/actions/list-sync-checkpoints?${params}`, {
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
      "baseRefBundles": [
        "string"
      ],
      "checkpoints": [
        "string"
      ],
      "headRefBundles": [
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
| `baseRefBundles` | array<string> |  |
| `checkpoints` | array<string> |  |
| `headRefBundles` | array<string> |  |

## Native endpoint

Through the native Omnara API, this operation is `GET /api/v1/workspaces/{workspaceId}/sync/checkpoints` (base URL `https://api.omnara.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-sync-checkpoints.md) for the provider-specific parameters and requirements.

