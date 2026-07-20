# Freshsales Classic: List All Appointments

Retrieves appointments from Freshsales Classic.

```
GET https://connect.mindcloud.co/v1/universal/freshsalesClassic/latest/actions/list-all-appointments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Freshsales Classic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/freshsalesClassic/latest/actions/list-all-appointments?connectionId=$CONNECTION_ID&filter=open" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "filter": "open"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/freshsalesClassic/latest/actions/list-all-appointments?${params}`, {
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
| `filter` | string | yes | Freshsales appointment filter. Use one documented filter at a time: open or complete. Default: `open`. Example: `open`. |
| `page` | number | no | Page number to return. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "createrId": 1,
      "description": "string",
      "endDate": "string",
      "fromDate": "string",
      "hasMultipleEmails": true,
      "id": 1,
      "isAllday": true,
      "location": "string",
      "outcomeId": 1,
      "provider": "string",
      "targetables": [
        {}
      ],
      "targetablesWithEmail": [
        {}
      ],
      "timeZone": "string",
      "title": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string | Appointment creation timestamp. |
| `createrId` | number | Creator user ID. |
| `description` | string | Appointment description. |
| `endDate` | string | Appointment end date and time. |
| `fromDate` | string | Appointment start date and time. |
| `hasMultipleEmails` | boolean | Whether multiple attendee emails are associated. |
| `id` | number | Appointment ID. |
| `isAllday` | boolean | Whether the appointment is all day. |
| `location` | string | Appointment location. |
| `outcomeId` | number | Appointment outcome ID. |
| `provider` | string | Appointment provider. |
| `targetables` | array<object> | Related target entities. |
| `targetablesWithEmail` | array<object> | Related target entities with names. |
| `timeZone` | string | Appointment time zone. |
| `title` | string | Appointment title. |
| `updatedAt` | string | Appointment update timestamp. |

## Native endpoint

Through the native Freshsales Classic API, this operation is `GET /appointments` (base URL `https://{{credentials.bundleAlias}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-all-appointments.md) for the provider-specific parameters and requirements.

