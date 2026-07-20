# Omnara: Enable Workspace Sync



```
PUT https://connect.mindcloud.co/v1/universal/omnara/latest/actions/enable-workspace-sync
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Omnara `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/omnara/latest/actions/enable-workspace-sync" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/omnara/latest/actions/enable-workspace-sync', {
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
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean |  |

## Native endpoint

Through the native Omnara API, this operation is `POST /api/v1/workspaces/{workspaceId}/sync/enable` (base URL `https://api.omnara.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/enable-workspace-sync.md) for the provider-specific parameters and requirements.

