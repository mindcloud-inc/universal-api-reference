# ClickMeeting: Get File

Retrieves a file from ClickMeeting by file ID.

```
GET https://connect.mindcloud.co/v1/universal/clickMeeting/latest/actions/get-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ClickMeeting `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clickMeeting/latest/actions/get-file?connectionId=$CONNECTION_ID&file_id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "file_id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clickMeeting/latest/actions/get-file?${params}`, {
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
| `file_id` | number | yes | File identifier. |

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

Through the native ClickMeeting API, this operation is `GET file-library/{{file_id}}` (base URL `https://api.clickmeeting.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-file.md) for the provider-specific parameters and requirements.

