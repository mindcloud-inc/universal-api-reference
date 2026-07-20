# Sessionize: List Schedule Days

Retrieves event schedule days from Sessionize.

```
GET https://connect.mindcloud.co/v1/universal/sessionize/latest/actions/list-schedule-days
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sessionize `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sessionize/latest/actions/list-schedule-days?connectionId=$CONNECTION_ID&endpointId=jl4ktls0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "endpointId": "jl4ktls0"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sessionize/latest/actions/list-schedule-days?${params}`, {
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
| `endpointId` | string | yes | Sessionize event API endpoint ID from URLs like https://sessionize.com/api/v2/{endpointId}/view/GridSmart. Default: `jl4ktls0`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "date": "2026-05-07T12:00:00.000Z",
      "isDefault": true,
      "rooms": [
        {}
      ],
      "timeSlots": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `date` | date | Schedule date. |
| `isDefault` | boolean | Whether this is the default schedule date. |
| `rooms` | array<object> | Rooms and sessions for the date. |
| `timeSlots` | array<object> | Time slots for the date. |

## Native endpoint

Through the native Sessionize API, this operation is `GET /api/v2/:endpointId/view/GridSmart` (base URL `https://sessionize.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-schedule-days.md) for the provider-specific parameters and requirements.

