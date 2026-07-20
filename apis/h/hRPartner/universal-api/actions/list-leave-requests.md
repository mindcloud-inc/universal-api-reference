# HR Partner: List Leave Requests



```
GET https://connect.mindcloud.co/v1/universal/hRPartner/latest/actions/list-leave-requests
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HR Partner `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hRPartner/latest/actions/list-leave-requests?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hRPartner/latest/actions/list-leave-requests?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "absenceReason": "string",
      "description": "string",
      "duration": 1,
      "employee": {},
      "id": 1,
      "leaveEndDate": "2026-05-07T12:00:00.000Z",
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
| `description` | string |  |
| `duration` | number |  |
| `employee` | object |  |
| `id` | number |  |
| `leaveEndDate` | date |  |
| `leaveRequestType` | string |  |
| `leaveStartDate` | date |  |
| `notes` | string |  |
| `reason` | string |  |
| `status` | string |  |
| `units` | string |  |

## Native endpoint

Through the native HR Partner API, this operation is `GET /leave_requests` (base URL `https://api.hrpartner.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-leave-requests.md) for the provider-specific parameters and requirements.

