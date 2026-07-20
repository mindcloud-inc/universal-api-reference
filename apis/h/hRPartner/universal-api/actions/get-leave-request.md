# HR Partner: Get Leave Request



```
GET https://connect.mindcloud.co/v1/universal/hRPartner/latest/actions/get-leave-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HR Partner `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hRPartner/latest/actions/get-leave-request?connectionId=$CONNECTION_ID&leaveRequestID=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "leaveRequestID": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hRPartner/latest/actions/get-leave-request?${params}`, {
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
| `leaveRequestID` | string | yes | Leave request ID from HR Partner. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "absenceReason": "string",
      "attachments": [
        {}
      ],
      "description": "string",
      "duration": 1,
      "employee": {},
      "id": 1,
      "leaveApprovalCondition": "string",
      "leaveEndDate": "2026-05-07T12:00:00.000Z",
      "leaveRequestActions": [
        {}
      ],
      "leaveRequestType": "string",
      "leaveStartDate": "2026-05-07T12:00:00.000Z",
      "notes": "string",
      "reason": "string",
      "status": "string",
      "units": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `absenceReason` | string |  |
| `attachments` | array<object> |  |
| `description` | string |  |
| `duration` | number |  |
| `employee` | object |  |
| `id` | number |  |
| `leaveApprovalCondition` | string |  |
| `leaveEndDate` | date |  |
| `leaveRequestActions` | array<object> |  |
| `leaveRequestType` | string |  |
| `leaveStartDate` | date |  |
| `notes` | string |  |
| `reason` | string |  |
| `status` | string |  |
| `units` | string |  |

## Native endpoint

Through the native HR Partner API, this operation is `GET /leave_request/:leaverequestID` (base URL `https://api.hrpartner.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-leave-request.md) for the provider-specific parameters and requirements.

