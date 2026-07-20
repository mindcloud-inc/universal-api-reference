# Zoho Calendar: Get User Free Busy Details

Retrieves user free/busy details from Zoho Calendar.

```
GET https://connect.mindcloud.co/v1/universal/zohoCalendar/latest/actions/get-user-free-busy-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Calendar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoCalendar/latest/actions/get-user-free-busy-details?connectionId=$CONNECTION_ID&userEmail=ava%40example.com&start=string&end=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "userEmail": "ava@example.com",
  "start": "string",
  "end": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoCalendar/latest/actions/get-user-free-busy-details?${params}`, {
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
| `userEmail` | string | yes | Email address of the user whose free/busy details you want. |
| `start` | string | yes | Start datetime in yyyyMMdd'T'HHmmss format. |
| `end` | string | yes | End datetime in yyyyMMdd'T'HHmmss format. |
| `freeBusyType` | string | no | Free/busy response style, for example eventbased or timebased. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "freebusy": [
        {
          "endTime": "2026-05-07T12:00:00.000Z",
          "fbtype": "string",
          "startTime": "2026-05-07T12:00:00.000Z"
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
| `freebusy[].endTime` | date |  |
| `freebusy[].fbtype` | string |  |
| `freebusy[].startTime` | date |  |

## Native endpoint

Through the native Zoho Calendar API, this operation is `GET /calendars/freebusy` (base URL `https://calendar.zoho.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-free-busy-details.md) for the provider-specific parameters and requirements.

