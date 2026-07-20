# Orufy Bookings: Get Event Availability



```
GET https://connect.mindcloud.co/v1/universal/orufyBookings/latest/actions/get-event-availability
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Orufy Bookings `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/orufyBookings/latest/actions/get-event-availability?connectionId=$CONNECTION_ID&accessLink=https%3A%2F%2Fexample.com&slug=string&timezone=string&start=2026-05-07T12%3A00%3A00.000Z&end=2026-05-07T12%3A00%3A00.000Z" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accessLink": "https://example.com",
  "slug": "string",
  "timezone": "string",
  "start": "2026-05-07T12:00:00.000Z",
  "end": "2026-05-07T12:00:00.000Z"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/orufyBookings/latest/actions/get-event-availability?${params}`, {
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
| `timezone` | string | yes | An IANA timezone, for example `America/Sao_Paulo`. |
| `start` | date | yes | The start date to check availability for, in ISO format. |
| `end` | date | yes | The end date to check availability for, in ISO format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "country": "string",
      "countryCode": "string",
      "days": {},
      "isSuccess": true,
      "maximumEnd": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `country` | string |  |
| `countryCode` | string |  |
| `days` | object |  |
| `isSuccess` | boolean |  |
| `maximumEnd` | date |  |

## Native endpoint

Through the native Orufy Bookings API, this operation is `POST /website/dates` (base URL `https://bookings.orufy.com/api/v1/bookings`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-event-availability.md) for the provider-specific parameters and requirements.

