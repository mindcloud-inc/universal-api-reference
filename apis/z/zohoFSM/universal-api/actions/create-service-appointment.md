# Zoho FSM: Create Service Appointment

Creates a new service appointment in Zoho FSM.

```
POST https://connect.mindcloud.co/v1/universal/zohoFSM/latest/actions/create-service-appointment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho FSM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoFSM/latest/actions/create-service-appointment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "data[0].Summary": "string",
  "data[0].Scheduled_Start_Date_Time": "string",
  "data[0].Scheduled_End_Date_Time": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoFSM/latest/actions/create-service-appointment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "data[0].Summary": "string",
    "data[0].Scheduled_Start_Date_Time": "string",
    "data[0].Scheduled_End_Date_Time": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `data[0].allow_overlapping` | boolean | no |  |
| `data[0].lead` | string | no |  |
| `data[0].service_resources[]` | array<string> | no |  |
| `data[0].service_tasks_line_items[]` | array<string> | no |  |
| `data[0].Summary` | string | yes | A summary for the service appointment. |
| `data[0].territory` | string | no |  |
| `data[0].Scheduled_Start_Date_Time` | string | yes | The scheduled start date time for the appointment. |
| `data[0].Scheduled_End_Date_Time` | string | yes | The scheduled end date time for the appointment. |
| `data[0].service_line_items[]` | array<string> | no | Service line item IDs to include in the appointment. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": "string",
      "data": [
        {
          "createdBy": {
            "id": "string",
            "name": "Ava Chen"
          },
          "createdTime": "2026-05-07T12:00:00.000Z",
          "id": "string",
          "modifiedBy": {
            "id": "string",
            "name": "Ava Chen"
          },
          "modifiedTime": "2026-05-07T12:00:00.000Z",
          "tabName": "Ava Chen",
          "uid": "string"
        }
      ],
      "result": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string |  |
| `data[].createdBy.id` | string |  |
| `data[].createdBy.name` | string |  |
| `data[].createdTime` | date |  |
| `data[].id` | string |  |
| `data[].modifiedBy.id` | string |  |
| `data[].modifiedBy.name` | string |  |
| `data[].modifiedTime` | date |  |
| `data[].tabName` | string |  |
| `data[].uid` | string |  |
| `result` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Zoho FSM API, this operation is `POST /Service_Appointments` (base URL `{{credentials.accessTokenRequest.api_domain}}/fsm/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-service-appointment.md) for the provider-specific parameters and requirements.

