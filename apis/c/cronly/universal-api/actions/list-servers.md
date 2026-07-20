# Cronly: List Servers



```
GET https://connect.mindcloud.co/v1/universal/cronly/latest/actions/list-servers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cronly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cronly/latest/actions/list-servers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cronly/latest/actions/list-servers?${params}`, {
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
      "company_id": 1,
      "created_at": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "identifier": "string",
      "ip_address": "string",
      "is_notified_on_backup": 1,
      "is_notified_on_new_backup_user": 1,
      "name": "Ava Chen",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `company_id` | number |  |
| `created_at` | date |  |
| `id` | number |  |
| `identifier` | string |  |
| `ip_address` | string |  |
| `is_notified_on_backup` | number |  |
| `is_notified_on_new_backup_user` | number |  |
| `name` | string |  |
| `updated_at` | date |  |

## Native endpoint

Through the native Cronly API, this operation is `GET /api/servers` (base URL `https://cronly.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-servers.md) for the provider-specific parameters and requirements.

