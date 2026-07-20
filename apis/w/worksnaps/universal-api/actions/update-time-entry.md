# Worksnaps: Update time entry

Updates an existing time entry in Worksnaps.

```
PUT https://connect.mindcloud.co/v1/universal/worksnaps/latest/actions/update-time-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Worksnaps `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/worksnaps/latest/actions/update-time-entry" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/worksnaps/latest/actions/update-time-entry', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `body` | string | no | Raw XML request body for this Worksnaps endpoint. |
| `project_id` | string | no | ID of the target project |
| `time_entry_id` | string | no | IDs of the target Time Entry to be updated, separated by semi-colon |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | number | Operation status. |

## Native endpoint

Through the native Worksnaps API, this operation is `PUT /projects/{project_id}/time_entries/{time_entry_id}.xml` (base URL `https://api.worksnaps.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-time-entry.md) for the provider-specific parameters and requirements.

