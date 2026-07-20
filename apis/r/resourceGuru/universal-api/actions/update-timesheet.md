# Resource Guru: Update Timesheet

Updates an existing timesheet in Resource Guru.

```
PUT https://connect.mindcloud.co/v1/universal/resourceGuru/latest/actions/update-timesheet
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Resource Guru `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/resourceGuru/latest/actions/update-timesheet" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "1"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/resourceGuru/latest/actions/update-timesheet', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "1"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | Timesheet ID. Default: `1`. Example: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "date": "string",
      "id": 1,
      "resource_id": 1,
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `date` | string | Timesheet date. |
| `id` | number | Timesheet ID. |
| `resource_id` | number | Resource ID. |
| `status` | string | Timesheet status. |

## Native endpoint

Through the native Resource Guru API, this operation is `PUT /timesheets/:id` (base URL `https://api.resourceguruapp.com/v1/{{credentials.accountId}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-timesheet.md) for the provider-specific parameters and requirements.

