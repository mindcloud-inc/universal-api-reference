# Zoho Calendar: Get Shared Calendar Details

Retrieves details for a shared calendar in Zoho Calendar.

```
GET https://connect.mindcloud.co/v1/universal/zohoCalendar/latest/actions/get-shared-calendar-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Calendar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoCalendar/latest/actions/get-shared-calendar-details?connectionId=$CONNECTION_ID&calendarUid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "calendarUid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoCalendar/latest/actions/get-shared-calendar-details?${params}`, {
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
| `calendarUid` | string | yes | Calendar unique identifier for the shared calendar. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "share": [
        {
          "emailid": "ava@example.com",
          "name": "Ava Chen",
          "privilege": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `share[].emailid` | string |  |
| `share[].name` | string |  |
| `share[].privilege` | string |  |

## Native endpoint

Through the native Zoho Calendar API, this operation is `GET /calendars/:calendaruid/share` (base URL `https://calendar.zoho.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-shared-calendar-details.md) for the provider-specific parameters and requirements.

