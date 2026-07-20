# Zoho People: Get Specific Leave Request

Retrieves a leave request from Zoho People.

```
GET https://connect.mindcloud.co/v1/universal/zohoPeople/latest/actions/get-specific-leave-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho People `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoPeople/latest/actions/get-specific-leave-request?connectionId=$CONNECTION_ID&recordId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "recordId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoPeople/latest/actions/get-specific-leave-request?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `recordId` | string | yes | Leave request record ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "approval_status": "string",
      "created_time": "string",
      "date_of_request": "string",
      "days": {},
      "employee": {
        "id": "string",
        "name": "Ava Chen",
        "zoho_id": 1
      },
      "from_date": "string",
      "leave_id": 1,
      "leave_type": {
        "id": 1,
        "name": "Ava Chen",
        "type": "string"
      },
      "modified_time": "string",
      "Reason": "string",
      "to_date": "string",
      "unit": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `approval_status` | string |  |
| `created_time` | string |  |
| `date_of_request` | string |  |
| `days` | object |  |
| `employee.id` | string |  |
| `employee.name` | string |  |
| `employee.zoho_id` | number |  |
| `from_date` | string |  |
| `leave_id` | number |  |
| `leave_type.id` | number |  |
| `leave_type.name` | string |  |
| `leave_type.type` | string |  |
| `modified_time` | string |  |
| `Reason` | string |  |
| `to_date` | string |  |
| `unit` | string |  |

## Native endpoint

Through the native Zoho People API, this operation is `GET /api/v3/leave-tracker/leaves/:recordId` (base URL `https://people.zoho.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-specific-leave-request.md) for the provider-specific parameters and requirements.

