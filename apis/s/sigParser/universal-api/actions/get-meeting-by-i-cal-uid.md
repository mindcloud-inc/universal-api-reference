# SigParser: Get Meeting By ICalUID



```
GET https://connect.mindcloud.co/v1/universal/sigParser/latest/actions/get-meeting-by-i-cal-uid
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SigParser `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sigParser/latest/actions/get-meeting-by-i-cal-uid?connectionId=$CONNECTION_ID&icalUid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "icalUid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sigParser/latest/actions/get-meeting-by-i-cal-uid?${params}`, {
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
| `icalUid` | string | yes | Meeting iCal UID to filter by. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attendees": [
        {}
      ],
      "cancelled": "string",
      "end": "string",
      "icaluid": "string",
      "icaluidDistinct": "string",
      "instanceType": "string",
      "lastmodified": 1,
      "location": "string",
      "mailboxInstance": {},
      "occurrences": [
        "string"
      ],
      "organizer": "string",
      "organizerName": "Ava Chen",
      "recurring": true,
      "sensitivity": "string",
      "showAs": "string",
      "start": "string",
      "subject": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attendees` | array<object> | Meeting attendees. |
| `cancelled` | string | Cancellation timestamp, when present. |
| `end` | string | Meeting end time. |
| `icaluid` | string | Meeting iCal UID. |
| `icaluidDistinct` | string | Distinct iCal UID for occurrences or exceptions. |
| `instanceType` | string | Meeting instance type. |
| `lastmodified` | number | Watermark for incremental meeting syncs. |
| `location` | string | Meeting location. |
| `mailboxInstance` | object | Mailbox instance metadata. |
| `occurrences` | array<string> | Occurrence timestamps for series masters. |
| `organizer` | string | Organizer email address. |
| `organizerName` | string | Organizer display name. |
| `recurring` | boolean | Whether the meeting is recurring. |
| `sensitivity` | string | Meeting sensitivity level. |
| `showAs` | string | Availability status for the meeting. |
| `start` | string | Meeting start time. |
| `subject` | string | Meeting subject. |

## Native endpoint

Through the native SigParser API, this operation is `GET /api/Meetings/Distinct` (base URL `https://ipaas.sigparser.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-meeting-by-i-cal-uid.md) for the provider-specific parameters and requirements.

