# Scanova: Update Lead List



```
PUT https://connect.mindcloud.co/v1/universal/scanova/latest/actions/update-lead-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scanova `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/scanova/latest/actions/update-lead-list" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "leadListId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/scanova/latest/actions/update-lead-list', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "leadListId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `leadListId` | string | yes | Lead list ID (lead_id) |
| `name` | string | no | Name of the lead list |
| `isActive` | boolean | no | Whether to activate or deactivate the lead list |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": "2026-05-07T12:00:00.000Z",
      "data": "string",
      "entries_count": 1,
      "id": 1,
      "is_active": true,
      "lead_id": "string",
      "linked_qrs": [
        {}
      ],
      "modified": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "usage_count": 1,
      "webhooks": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | date |  |
| `data` | string |  |
| `entries_count` | number |  |
| `id` | number |  |
| `is_active` | boolean |  |
| `lead_id` | string |  |
| `linked_qrs` | array<object> |  |
| `modified` | date |  |
| `name` | string |  |
| `usage_count` | number |  |
| `webhooks` | array<object> |  |

## Native endpoint

Through the native Scanova API, this operation is `PATCH /lead/{lead_list_id}/` (base URL `https://management.scanova.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-lead-list.md) for the provider-specific parameters and requirements.

