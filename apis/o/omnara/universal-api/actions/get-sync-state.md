# Omnara: Get Sync State



```
GET https://connect.mindcloud.co/v1/universal/omnara/latest/actions/get-sync-state
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Omnara `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/omnara/latest/actions/get-sync-state?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/omnara/latest/actions/get-sync-state?${params}`, {
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
      "lastBaseRefSyncAt": "string",
      "lastBaseRefSyncRef": "string",
      "lastBaseRefSyncSha": "string",
      "syncedCheckpoints": [
        "string"
      ],
      "syncedHeadRefs": [
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
| `lastBaseRefSyncAt` | string |  |
| `lastBaseRefSyncRef` | string |  |
| `lastBaseRefSyncSha` | string |  |
| `syncedCheckpoints` | array<string> |  |
| `syncedHeadRefs` | array<string> |  |

## Native endpoint

Through the native Omnara API, this operation is `GET /api/v1/workspaces/{workspaceId}/sync/state` (base URL `https://api.omnara.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-sync-state.md) for the provider-specific parameters and requirements.

