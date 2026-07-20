# MILKEE: Update Time Entry

Updates an existing time entry in MILKEE.

```
PUT https://connect.mindcloud.co/v1/universal/mILKEE/latest/actions/update-time-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MILKEE `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/mILKEE/latest/actions/update-time-entry" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "companyId": "4640",
  "timeId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mILKEE/latest/actions/update-time-entry', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "companyId": "4640",
    "timeId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `billable` | boolean | no | Whether the time is billable. |
| `companyId` | string | yes | The numeric MILKEE company ID used in the request path. Default: `4640`. |
| `date` | string | no | Date of work. |
| `description` | string | no | Description of work performed. |
| `end` | string | no | End time in H:i format. |
| `force` | boolean | no | Force update of invoiced entries. |
| `hourlyRate` | number | no | Hourly rate for the entry. |
| `hours` | number | no | Hours worked. |
| `invoiceId` | number | no | Associated invoice ID. |
| `minutes` | number | no | Minutes worked. |
| `projectId` | number | no | ID of the project. |
| `start` | string | no | Start time in H:i format. |
| `status` | string | no | Time entry status: open, invoiced, or paid. |
| `taskId` | number | no | Associated task ID. |
| `timeId` | string | yes | The numeric MILKEE time entry ID used in the request path. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |

## Native endpoint

Through the native MILKEE API, this operation is `PUT /companies/:companyId/times/:timeId` (base URL `https://app.milkee.ch/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-time-entry.md) for the provider-specific parameters and requirements.

