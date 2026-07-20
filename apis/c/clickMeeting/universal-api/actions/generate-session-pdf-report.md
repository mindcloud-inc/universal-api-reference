# ClickMeeting: Generate Session PDF Report

Generates a session PDF report in ClickMeeting.

```
GET https://connect.mindcloud.co/v1/universal/clickMeeting/latest/actions/generate-session-pdf-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ClickMeeting `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clickMeeting/latest/actions/generate-session-pdf-report?connectionId=$CONNECTION_ID&room_id=1&session_id=1&lang=en" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "room_id": "1",
  "session_id": "1",
  "lang": "en"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clickMeeting/latest/actions/generate-session-pdf-report?${params}`, {
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
| `lang` | string | yes | Report language token from ClickMeeting. Default: `en`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "progress": 1,
      "status": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `progress` | number | PDF generation progress percentage. |
| `status` | string | PDF generation status. |
| `url` | string | Generated PDF download URL. |

## Native endpoint

Through the native ClickMeeting API, this operation is `GET conferences/{{room_id}}/sessions/{{session_id}}/generate-pdf/{{lang}}` (base URL `https://api.clickmeeting.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-session-pdf-report.md) for the provider-specific parameters and requirements.

