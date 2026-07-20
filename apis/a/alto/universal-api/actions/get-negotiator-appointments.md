# Alto: Get Negotiator Appointments

Retrieves negotiator appointments from Alto within a selected time range.

```
GET https://connect.mindcloud.co/v1/universal/alto/latest/actions/get-negotiator-appointments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Alto `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/alto/latest/actions/get-negotiator-appointments?connectionId=$CONNECTION_ID&limit=25&offset=0&startDate=2026-05-07T12%3A00%3A00.000Z&endDate=2026-05-07T12%3A00%3A00.000Z&negotiatorId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "startDate": "2026-05-07T12:00:00.000Z",
  "endDate": "2026-05-07T12:00:00.000Z",
  "negotiatorId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/alto/latest/actions/get-negotiator-appointments?${params}`, {
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
| `startDate` | date | yes | Start of the appointment date range. |
| `endDate` | date | yes | End of the appointment date range. |
| `negotiatorId` | string | yes | Negotiator identifier whose appointments should be returned. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "appointments": [
        {}
      ],
      "negotiatorId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `appointments` | array<object> |  |
| `negotiatorId` | number |  |

## Native endpoint

Through the native Alto API, this operation is `GET /appointments/negotiators` (base URL `https://api.alto.zoopladev.co.uk`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-negotiator-appointments.md) for the provider-specific parameters and requirements.

