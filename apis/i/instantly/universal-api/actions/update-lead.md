# Instantly: Update Lead

Updates an existing lead in Instantly.

```
PUT https://connect.mindcloud.co/v1/universal/instantly/latest/actions/update-lead
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instantly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/instantly/latest/actions/update-lead" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/instantly/latest/actions/update-lead', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Lead ID. |
| `firstName` | string | no | Updated first name. |
| `lastName` | string | no | Updated last name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "company_name": "Ava Chen",
      "email": "ava@example.com",
      "first_name": "Ava",
      "id": "string",
      "last_name": "Chen",
      "list_id": "string",
      "organization": "string",
      "status": 1,
      "timestamp_created": "2026-05-07T12:00:00.000Z",
      "timestamp_updated": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `company_name` | string |  |
| `email` | string |  |
| `first_name` | string |  |
| `id` | string |  |
| `last_name` | string |  |
| `list_id` | string |  |
| `organization` | string |  |
| `status` | number |  |
| `timestamp_created` | date |  |
| `timestamp_updated` | date |  |

## Native endpoint

Through the native Instantly API, this operation is `PATCH /api/v2/leads/:id` (base URL `https://api.instantly.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-lead.md) for the provider-specific parameters and requirements.

