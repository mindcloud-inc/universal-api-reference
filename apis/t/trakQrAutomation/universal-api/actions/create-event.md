# Trak Qr Automation: Create Event

Creates a new event in Trak Qr Automation.

```
POST https://connect.mindcloud.co/v1/universal/trakQrAutomation/latest/actions/create-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Trak Qr Automation `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/trakQrAutomation/latest/actions/create-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "title": "string",
  "eventId": "string",
  "formFields[]": [
    {}
  ],
  "formFields[].name": "Ava Chen",
  "formFields[].editor": "0"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/trakQrAutomation/latest/actions/create-event', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "title": "string",
    "eventId": "string",
    "formFields[]": [{}],
    "formFields[].name": "Ava Chen",
    "formFields[].editor": "0"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `title` | string | yes | Event user-facing name, used as app title in Trak. |
| `eventId` | string | yes | Your internal event ID, used as correlation ID. |
| `formFields[]` | array<object> | yes | Schema of attendee attachment fields for this event. |
| `formFields[].name` | string | yes | Field name used as label and report column header. |
| `formFields[].editor` | list | yes | Field type: number, line, text, select, radios, or checkboxes. One of: `0`, `1`, `2`, `3`, `4`, `5`. |
| `formFields[].values[]` | array<string> | no | Allowed values for select, radios, and checkboxes fields. Accepts multiple values as an array. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `titleFormat` | string | no | Mini-template for ticket titles, such as {First name} {Last name}. |
| `logoUrl` | string | no | Optional PNG or JPG logo URL for tickets, ideally 300x300px with a white background. |
| `bgUrl` | string | no | Optional PNG or JPG ticket background URL, ideally 596x842px. |
| `creatorInfo` | object | no | Optional information about the form creator. |
| `creatorInfo.ip` | string | no | Creator IP address. |
| `creatorInfo.loc` | string | no | Creator country or town. |
| `creatorInfo.email` | string | no | Creator email used for support. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "eventId": "string",
      "eventKey": "string",
      "urls": {
        "access": "https://example.com",
        "allReport": "https://example.com",
        "cancel": "https://example.com",
        "canceledReport": "https://example.com",
        "checkedInReport": "https://example.com",
        "checkIn": "https://example.com",
        "csvCheckInReport": "https://example.com",
        "dashboard": "https://example.com",
        "designer": "https://example.com",
        "lookup": "https://example.com",
        "notCheckedInReport": "https://example.com",
        "pay": "https://example.com",
        "register": "https://example.com",
        "scanCountsReport": "https://example.com"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `eventId` | string | Internal event ID from the request. |
| `eventKey` | string | Generated Trak event key used when creating attendees. |
| `urls.access` | string |  |
| `urls.allReport` | string |  |
| `urls.cancel` | string |  |
| `urls.canceledReport` | string |  |
| `urls.checkedInReport` | string |  |
| `urls.checkIn` | string |  |
| `urls.csvCheckInReport` | string |  |
| `urls.dashboard` | string |  |
| `urls.designer` | string |  |
| `urls.lookup` | string |  |
| `urls.notCheckedInReport` | string |  |
| `urls.pay` | string |  |
| `urls.register` | string |  |
| `urls.scanCountsReport` | string |  |

## Native endpoint

Through the native Trak Qr Automation API, this operation is `POST /events` (base URL `https://backend.trak.codes/api/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-event.md) for the provider-specific parameters and requirements.

