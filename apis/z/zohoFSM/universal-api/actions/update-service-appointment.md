# Zoho FSM: Update Service Appointment

Updates an existing service appointment in Zoho FSM.

```
PUT https://connect.mindcloud.co/v1/universal/zohoFSM/latest/actions/update-service-appointment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho FSM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/zohoFSM/latest/actions/update-service-appointment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "data[0].appointments_x_services[].service_line_item.id": "string",
  "data[0].id": "string",
  "data[0].appointments_x_services[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoFSM/latest/actions/update-service-appointment', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "data[0].appointments_x_services[].service_line_item.id": "string",
    "data[0].id": "string",
    "data[0].appointments_x_services[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `data[0].appointments_x_services[].contact.id` | string | no |  |
| `data[0].appointments_x_services[].id` | string | no |  |
| `data[0].appointments_x_services[].name` | string | no |  |
| `data[0].appointments_x_services[].service_line_item.id` | string | yes | The service line item ID inside the appointment-service relationship. |
| `data[0].appointments_x_services[].service_task_line_item.id` | string | no |  |
| `data[0].appointments_x_services[].sli_status` | string | no |  |
| `data[0].appointments_x_services[].stli_status` | string | no |  |
| `data[0].appointments_x_services[].work_order.id` | string | no |  |
| `data[0].id` | string | yes | The unique ID of the record. |
| `data[0].Summary` | string | no | A summary for the service appointment. |
| `data[0].appointments_x_services[]` | array<object> | yes | Appointment-service relationship objects to update on the service appointment. |

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

Through the native Zoho FSM API, this operation is `PUT /Service_Appointments` (base URL `{{credentials.accessTokenRequest.api_domain}}/fsm/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-service-appointment.md) for the provider-specific parameters and requirements.

