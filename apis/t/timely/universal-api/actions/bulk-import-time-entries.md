# Timely: Bulk Import Time Entries

Creates a bulk import job for time entries in Timely.

```
POST https://connect.mindcloud.co/v1/universal/timely/latest/actions/bulk-import-time-entries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timely `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/timely/latest/actions/bulk-import-time-entries" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accountId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/timely/latest/actions/bulk-import-time-entries', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accountId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accountId` | number | yes | Workspace id |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `create[]` | array<object> | no | Array of time entries to create. Each item accepts all standard event/time entry fields from PayloadSchema. |
| `update[]` | array<object> | no | Array of time entries to update. Must include id field. All other fields from UpdatePayloadSchema are optional. |
| `delete[]` | array<number> | no | Array of time entry IDs to delete |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_ids": [
        1
      ],
      "deleted_ids": [
        1
      ],
      "errors": {},
      "job": {},
      "updated_ids": [
        1
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_ids` | array<number> |  |
| `deleted_ids` | array<number> |  |
| `errors` | object |  |
| `job` | object |  |
| `updated_ids` | array<number> |  |

## Native endpoint

Through the native Timely API, this operation is `POST /1.1/{account_id}/bulk/hours` (base URL `https://api.timelyapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/bulk-import-time-entries.md) for the provider-specific parameters and requirements.

