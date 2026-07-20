# Xano: Set Live Branch

Sets a branch as live in Xano.

```
PUT https://connect.mindcloud.co/v1/universal/xano/latest/actions/set-live-branch
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Xano `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/xano/latest/actions/set-live-branch" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "branch_label": "string",
  "workspace_id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/xano/latest/actions/set-live-branch', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "branch_label": "string",
    "workspace_id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `branch_label` | string | yes |  |
| `workspace_id` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "backup": true,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "label": "string",
      "live": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `backup` | boolean |  |
| `createdAt` | date |  |
| `id` | number |  |
| `label` | string |  |
| `live` | boolean |  |

## Native endpoint

Through the native Xano API, this operation is `POST /api%3Ameta/workspace/:workspace_id/branch/:branch_label/live` (base URL `https://x8ki-letl-twmt.n7.xano.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/set-live-branch.md) for the provider-specific parameters and requirements.

