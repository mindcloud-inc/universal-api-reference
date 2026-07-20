# Instantly: Merge Leads

Merges two leads in Instantly.

```
PUT https://connect.mindcloud.co/v1/universal/instantly/latest/actions/merge-leads
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instantly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/instantly/latest/actions/merge-leads" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "leadId": "string",
  "destinationLeadId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/instantly/latest/actions/merge-leads', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "leadId": "string",
    "destinationLeadId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `leadId` | string | yes | ID of the lead to merge. |
| `destinationLeadId` | string | yes | ID of the destination lead to merge into. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assigned_to": "string",
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
| `assigned_to` | string |  |
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

Through the native Instantly API, this operation is `POST /api/v2/leads/merge` (base URL `https://api.instantly.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/merge-leads.md) for the provider-specific parameters and requirements.

