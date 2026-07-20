# serviceminder.io: Query Appointments

Finds appointments in ServiceMinder by date, contact, or agent.

```
GET https://connect.mindcloud.co/v1/universal/serviceminderio/latest/actions/query-appointments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a serviceminder.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/serviceminderio/latest/actions/query-appointments?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/serviceminderio/latest/actions/query-appointments?${params}`, {
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
| `fromDate` | date | no | Start date for appointment query. |
| `throughDate` | date | no | End date for appointment query. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contactId` | number | no | Filter by contact identifier. |
| `serviceAgentId` | number | no | Filter by service agent identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "appointments": [
        {}
      ],
      "count": 1,
      "message": "string",
      "resultCode": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `appointments` | array<object> |  |
| `count` | number |  |
| `message` | string |  |
| `resultCode` | number |  |

## Native endpoint

Through the native serviceminder.io API, this operation is `POST /appointments/query` (base URL `https://serviceminder.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/query-appointments.md) for the provider-specific parameters and requirements.

