# ClickMeeting: Delete All Conference Recordings

Deletes all conference recordings from ClickMeeting.

```
DELETE https://connect.mindcloud.co/v1/universal/clickMeeting/latest/actions/delete-all-conference-recordings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ClickMeeting `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/clickMeeting/latest/actions/delete-all-conference-recordings?connectionId=$CONNECTION_ID&room_id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "room_id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clickMeeting/latest/actions/delete-all-conference-recordings?${params}`, {
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
      "STATUS": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `STATUS` | string | Deletion result. |

## Native endpoint

Through the native ClickMeeting API, this operation is `DELETE conferences/{{room_id}}/recordings` (base URL `https://api.clickmeeting.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-all-conference-recordings.md) for the provider-specific parameters and requirements.

