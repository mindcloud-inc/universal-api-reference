# Omnara: Update Sync State



```
PUT https://connect.mindcloud.co/v1/universal/omnara/latest/actions/update-sync-state
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Omnara `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/omnara/latest/actions/update-sync-state" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/omnara/latest/actions/update-sync-state', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
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

Through the native Omnara API, this operation is `PATCH /api/v1/workspaces/{workspaceId}/sync/state` (base URL `https://api.omnara.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-sync-state.md) for the provider-specific parameters and requirements.

