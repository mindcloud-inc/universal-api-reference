# Supabase: List Audit Logs



```
GET https://connect.mindcloud.co/v1/universal/supabase/latest/actions/list-audit-logs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Supabase `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/supabase/latest/actions/list-audit-logs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/supabase/latest/actions/list-audit-logs?${params}`, {
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
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "ipAddress": "string",
      "payload": {
        "action": "string",
        "actorId": "string",
        "actorName": "Ava Chen",
        "actorUsername": "Ava Chen",
        "actorViaSso": true,
        "logType": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `id` | string |  |
| `ipAddress` | string |  |
| `payload` | object |  |
| `payload.action` | string |  |
| `payload.actorId` | string |  |
| `payload.actorName` | string |  |
| `payload.actorUsername` | string |  |
| `payload.actorViaSso` | boolean |  |
| `payload.logType` | string |  |

## Native endpoint

Through the native Supabase API, this operation is `GET /auth/v1/admin/audit` (base URL `{{credentials.projectUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-audit-logs.md) for the provider-specific parameters and requirements.

