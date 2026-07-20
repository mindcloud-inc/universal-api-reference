# Cerbo: Get Appointment Availability

Retrieves appointment availability from Cerbo.

```
GET https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/get-appointment-availability
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cerbo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/get-appointment-availability?connectionId=$CONNECTION_ID&start_date=string&end_date=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "start_date": "string",
  "end_date": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/get-appointment-availability?${params}`, {
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
| `start_date` | string | yes | Starting date of the date range. The start date should be formatted as `YYYY-MM-DD`. |
| `end_date` | string | yes | Ending date of the date range. The end date should be formatted as `YYYY-MM-DD`. The end date cannot be more than 90 days from the start date. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `provider_ids[]` | array<number> | no | Provider identifiers. If specified, results will be for only those providers. |
| `appointment_type_ids[]` | array<number> | no | Appointment type identifiers. If specified, results will be for only those appointment types. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "availability_by_type": [
        {}
      ],
      "provider_details": {},
      "provider_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `availability_by_type` | array<object> |  |
| `provider_details` | object |  |
| `provider_id` | number |  |

## Native endpoint

Through the native Cerbo API, this operation is `GET /appointments/availability` (base URL `https://{{credentials.tenant}}.md-hq.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-appointment-availability.md) for the provider-specific parameters and requirements.

