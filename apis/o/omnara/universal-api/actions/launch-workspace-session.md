# Omnara: Launch Workspace Session



```
POST https://connect.mindcloud.co/v1/universal/omnara/latest/actions/launch-workspace-session
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Omnara `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/omnara/latest/actions/launch-workspace-session" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/omnara/latest/actions/launch-workspace-session', {
  method: 'POST',
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
      "payload": {},
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `payload` | object |  |
| `status` | string |  |

## Native endpoint

Through the native Omnara API, this operation is `POST /api/v1/workspaces/{workspaceId}/sessions` (base URL `https://api.omnara.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/launch-workspace-session.md) for the provider-specific parameters and requirements.

