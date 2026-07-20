# ClickMeeting: Upload Conference File

Creates a conference file in ClickMeeting.

```
POST https://connect.mindcloud.co/v1/universal/clickMeeting/latest/actions/upload-conference-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ClickMeeting `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/clickMeeting/latest/actions/upload-conference-file" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "room_id": 1,
  "uploaded": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clickMeeting/latest/actions/upload-conference-file', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "room_id": 1,
    "uploaded": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `room_id` | number | yes | Conference room identifier. |
| `uploaded` | file | yes | File to upload into the conference library. |

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
| `id` | number | Uploaded file identifier. |
| `name` | string | Uploaded file name. |
| `status` | string | Conversion status. |
| `upload_date` | date | Upload timestamp. |
| `url` | string | File download URL. |

## Native endpoint

Through the native ClickMeeting API, this operation is `POST file-library/conferences/{{room_id}}` (base URL `https://api.clickmeeting.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-conference-file.md) for the provider-specific parameters and requirements.

