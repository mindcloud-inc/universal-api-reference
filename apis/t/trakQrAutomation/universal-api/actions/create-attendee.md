# Trak Qr Automation: Create Attendee

Creates a new attendee for an event in Trak Qr Automation.

```
POST https://connect.mindcloud.co/v1/universal/trakQrAutomation/latest/actions/create-attendee
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Trak Qr Automation `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/trakQrAutomation/latest/actions/create-attendee" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "eventKey": "string",
  "attachments[]": [
    {}
  ],
  "attachments[].kind": "string",
  "attachments[].val": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/trakQrAutomation/latest/actions/create-attendee', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "eventKey": "string",
    "attachments[]": [{}],
    "attachments[].kind": "string",
    "attachments[].val": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `eventKey` | string | yes | Generated event key returned by Create Event. |
| `notes` | string | no | Optional comments on the attendee. |
| `attachments[]` | array<object> | yes | Attendee form data fields. |
| `attachments[].kind` | string | yes | Attachment field name matching an event form field. |
| `attachments[].val` | string | yes | Attachment field value. Trak accepts a number, string, or string array. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `attachments[].internal` | boolean | no | Set true for technical fields that should not be shown in the Trak UI. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "pdfUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `pdfUrl` | string | URL for downloading the PDF ticket. Append &inline=true to display it in browser. |

## Native endpoint

Through the native Trak Qr Automation API, this operation is `POST /events/:eventKey/attendees` (base URL `https://backend.trak.codes/api/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-attendee.md) for the provider-specific parameters and requirements.

