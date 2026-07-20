# Cal.com: Get Event Type

Retrieves an event type from Cal.com.

```
GET https://connect.mindcloud.co/v1/universal/cal/latest/actions/get-event-type
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cal.com `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cal/latest/actions/get-event-type?connectionId=$CONNECTION_ID&eventTypeId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "eventTypeId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cal/latest/actions/get-event-type?${params}`, {
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
| `eventTypeId` | list | yes | Event type identifier from Cal.com path parameter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bookingUrl": "https://example.com",
      "currency": "string",
      "description": "string",
      "hidden": true,
      "id": 1,
      "lengthInMinutes": 1,
      "locations": [
        {}
      ],
      "metadata": {},
      "scheduleId": 1,
      "slug": "string",
      "title": "string",
      "users": [
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
| `bookingUrl` | string |  |
| `currency` | string |  |
| `description` | string |  |
| `hidden` | boolean |  |
| `id` | number |  |
| `lengthInMinutes` | number |  |
| `locations` | array<object> |  |
| `metadata` | object |  |
| `scheduleId` | number |  |
| `slug` | string |  |
| `title` | string |  |
| `users` | array<object> |  |

## Native endpoint

Through the native Cal.com API, this operation is `GET /event-types/:eventTypeId` (base URL `https://api.cal.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-event-type.md) for the provider-specific parameters and requirements.

