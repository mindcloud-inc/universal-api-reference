# ClickMeeting: List Conference Files

Retrieves files for a conference in ClickMeeting.

```
GET https://connect.mindcloud.co/v1/universal/clickMeeting/latest/actions/list-conference-files
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ClickMeeting `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clickMeeting/latest/actions/list-conference-files?connectionId=$CONNECTION_ID&room_id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "room_id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clickMeeting/latest/actions/list-conference-files?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "conversion_progress": 1,
      "document_type": "string",
      "id": 1,
      "name": "Ava Chen",
      "status": "string",
      "status_message": "string",
      "upload_date": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `conversion_progress` | number | Conversion progress percentage. |
| `document_type` | string | Document type. |
| `id` | number | File identifier. |
| `name` | string | File name. |
| `status` | string | Conversion status. |
| `status_message` | string | Conversion status message. |
| `upload_date` | date | Upload timestamp. |
| `url` | string | File download URL. |

## Native endpoint

Through the native ClickMeeting API, this operation is `GET file-library/conferences/{{room_id}}` (base URL `https://api.clickmeeting.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-conference-files.md) for the provider-specific parameters and requirements.

