# Zoho People: Update Leave Request

Updates a leave request in Zoho People.

```
PUT https://connect.mindcloud.co/v1/universal/zohoPeople/latest/actions/update-leave-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho People `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/zohoPeople/latest/actions/update-leave-request" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "leaveRecordId": "string",
  "employeeZohoId": "string",
  "leaveTypeId": "string",
  "fromDate": "string",
  "toDate": "string",
  "unit": "Days"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoPeople/latest/actions/update-leave-request', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "leaveRecordId": "string",
    "employeeZohoId": "string",
    "leaveTypeId": "string",
    "fromDate": "string",
    "toDate": "string",
    "unit": "Days"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `leaveRecordId` | string | yes | Leave request record ID to update. |
| `employeeZohoId` | string | yes | Zoho employee erecno for the leave request. |
| `leaveTypeId` | string | yes | Zoho leave type ID. |
| `fromDate` | string | yes | Leave start date in the organization date format. |
| `toDate` | string | yes | Leave end date in the organization date format. |
| `unit` | string | yes | Leave unit. Zoho documents Days or Hours. Default: `Days`. |
| `reason` | string | no | Optional reason for the leave request. |
| `days` | string | no | Optional JSON object keyed by date with leave_count, session, start_time, and end_time. |
| `approverId` | string | no | Optional approver erecno when employees choose an approver. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "id": 1
      },
      "message": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.id` | number | Updated leave request identifier returned by Zoho. |
| `message` | string | Provider success message. |
| `status` | string | Provider status string. |

## Native endpoint

Through the native Zoho People API, this operation is `PUT /api/v3/leave-tracker/leaves/:leaveRecordId` (base URL `https://people.zoho.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-leave-request.md) for the provider-specific parameters and requirements.

