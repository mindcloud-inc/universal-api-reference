# ClickMeeting: Download File

Downloads a file from ClickMeeting by file ID.

```
GET https://connect.mindcloud.co/v1/universal/clickMeeting/latest/actions/download-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ClickMeeting `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clickMeeting/latest/actions/download-file?connectionId=$CONNECTION_ID&file_id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "file_id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clickMeeting/latest/actions/download-file?${params}`, {
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

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ClickMeeting API returns.

## Native endpoint

Through the native ClickMeeting API, this operation is `GET file-library/{{file_id}}/download` (base URL `https://api.clickmeeting.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/download-file.md) for the provider-specific parameters and requirements.

