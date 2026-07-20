# Cronly: Create SSL Certificate Monitor



```
POST https://connect.mindcloud.co/v1/universal/cronly/latest/actions/create-ssl-certificate-monitor
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cronly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cronly/latest/actions/create-ssl-certificate-monitor" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "hostname": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cronly/latest/actions/create-ssl-certificate-monitor', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "hostname": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `hostname` | string | yes | Hostname of the SSL certificate monitor. |
| `port` | number | no | Port to check. Defaults to 443. Default: `443`. |
| `projectId` | number | no | Optional project to associate with the certificate monitor. |

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

Through the native Cronly API, this operation is `POST /api/certificates` (base URL `https://cronly.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-ssl-certificate-monitor.md) for the provider-specific parameters and requirements.

