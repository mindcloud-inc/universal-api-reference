# ClickMeeting: Get Conference Session

Retrieves a conference session from ClickMeeting.

```
GET https://connect.mindcloud.co/v1/universal/clickMeeting/latest/actions/get-conference-session
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ClickMeeting `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clickMeeting/latest/actions/get-conference-session?connectionId=$CONNECTION_ID&room_id=1&session_id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "room_id": "1",
  "session_id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clickMeeting/latest/actions/get-conference-session?${params}`, {
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
| `room_id` | number | yes | Conference room identifier. |
| `session_id` | number | yes | Session identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attendees": [
        {}
      ],
      "end_date": "2026-05-07T12:00:00.000Z",
      "max_visitors": 1,
      "pdf": {
        "en": {
          "generate_pdf_url": "https://example.com",
          "progress": 1
        }
      },
      "start_date": "2026-05-07T12:00:00.000Z",
      "total_visitors": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attendees` | array<object> | Session attendees. |
| `end_date` | date | Session end timestamp. |
| `max_visitors` | number | Maximum concurrent visitors. |
| `pdf.en.generate_pdf_url` | string | English PDF generation URL. |
| `pdf.en.progress` | number | English PDF generation progress. |
| `start_date` | date | Session start timestamp. |
| `total_visitors` | number | Total visitors recorded for the session. |

## Native endpoint

Through the native ClickMeeting API, this operation is `GET conferences/{{room_id}}/sessions/{{session_id}}` (base URL `https://api.clickmeeting.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-conference-session.md) for the provider-specific parameters and requirements.

