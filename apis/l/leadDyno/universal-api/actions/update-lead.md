# LeadDyno: Update Lead

Updates an existing lead in LeadDyno.

```
PUT https://connect.mindcloud.co/v1/universal/leadDyno/latest/actions/update-lead
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LeadDyno `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/leadDyno/latest/actions/update-lead" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/leadDyno/latest/actions/update-lead', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
    "email": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `first_name` | string | no | The first name of the lead. |
| `id` | number | yes | The lead ID. |
| `last_name` | string | no | The last name of the lead. |
| `email` | string | yes | The email address of the lead. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "affiliate": {},
      "campaign": {},
      "created_at": "string",
      "email": "ava@example.com",
      "first_name": "Ava",
      "id": 1,
      "last_name": "Chen",
      "latest_visitor": {},
      "status": "string",
      "tracking_code": "string",
      "updated_at": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `affiliate` | object |  |
| `campaign` | object |  |
| `created_at` | string |  |
| `email` | string |  |
| `first_name` | string |  |
| `id` | number |  |
| `last_name` | string |  |
| `latest_visitor` | object |  |
| `status` | string |  |
| `tracking_code` | string |  |
| `updated_at` | string |  |

## Native endpoint

Through the native LeadDyno API, this operation is `PUT /leads/:id` (base URL `https://api.leaddyno.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-lead.md) for the provider-specific parameters and requirements.

