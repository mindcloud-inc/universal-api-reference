# Orufy Bookings: Get Public Event



```
GET https://connect.mindcloud.co/v1/universal/orufyBookings/latest/actions/get-public-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Orufy Bookings `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/orufyBookings/latest/actions/get-public-event?connectionId=$CONNECTION_ID&accessLink=https%3A%2F%2Fexample.com&slug=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accessLink": "https://example.com",
  "slug": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/orufyBookings/latest/actions/get-public-event?${params}`, {
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
| `accessLink` | string | yes | The Orufy access link, for example `mindcloud`. |
| `slug` | string | yes | The public event slug, for example `30-min-intro-call`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "agentsDetails": [
        {}
      ],
      "description": "string",
      "duration": 1,
      "Id": "string",
      "location": "string",
      "name": "Ava Chen",
      "questions": [
        {}
      ],
      "schedule": {},
      "slug": "string",
      "status": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `agentsDetails` | array<object> |  |
| `description` | string |  |
| `duration` | number |  |
| `Id` | string |  |
| `location` | string |  |
| `name` | string |  |
| `questions` | array<object> |  |
| `schedule` | object |  |
| `slug` | string |  |
| `status` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Orufy Bookings API, this operation is `GET /website/event/:accessLink/:slug` (base URL `https://bookings.orufy.com/api/v1/bookings`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-public-event.md) for the provider-specific parameters and requirements.

