# Cronly: Get SSL Certificate Monitor



```
GET https://connect.mindcloud.co/v1/universal/cronly/latest/actions/get-ssl-certificate-monitor
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cronly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cronly/latest/actions/get-ssl-certificate-monitor?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cronly/latest/actions/get-ssl-certificate-monitor?${params}`, {
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
| `id` | number | yes | The ID of the SSL certificate monitor to view. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "company_id": 1,
      "created_at": "2026-05-07T12:00:00.000Z",
      "expires_at": "2026-05-07T12:00:00.000Z",
      "hostname": "Ava Chen",
      "id": 1,
      "last_checked_at": "2026-05-07T12:00:00.000Z",
      "port": 1,
      "project_id": 1,
      "status": "string",
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
| `expires_at` | date |  |
| `hostname` | string |  |
| `id` | number |  |
| `last_checked_at` | date |  |
| `port` | number |  |
| `project_id` | number |  |
| `status` | string |  |
| `updated_at` | date |  |

## Native endpoint

Through the native Cronly API, this operation is `GET /api/certificates/:id` (base URL `https://cronly.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-ssl-certificate-monitor.md) for the provider-specific parameters and requirements.

