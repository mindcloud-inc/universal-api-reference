# Alto: Get Appointment

Retrieves an appointment from Alto by ID and instance.

```
GET https://connect.mindcloud.co/v1/universal/alto/latest/actions/get-appointment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Alto `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/alto/latest/actions/get-appointment?connectionId=$CONNECTION_ID&appointmentId=string&instanceId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "appointmentId": "string",
  "instanceId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/alto/latest/actions/get-appointment?${params}`, {
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
| `appointmentId` | string | yes | Unique Alto appointment identifier. |
| `instanceId` | number | yes | Numeric appointment instance identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "endDate": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "instanceId": 1,
      "isCancelled": true,
      "startDate": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "title": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `endDate` | date |  |
| `id` | number |  |
| `instanceId` | number |  |
| `isCancelled` | boolean |  |
| `startDate` | date |  |
| `status` | string |  |
| `title` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Alto API, this operation is `GET /appointments/:appointmentId/:instanceId` (base URL `https://api.alto.zoopladev.co.uk`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-appointment.md) for the provider-specific parameters and requirements.

