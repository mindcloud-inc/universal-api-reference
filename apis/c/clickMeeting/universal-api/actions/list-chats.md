# ClickMeeting: List Chats

Retrieves chat archives from ClickMeeting sessions.

```
GET https://connect.mindcloud.co/v1/universal/clickMeeting/latest/actions/list-chats
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ClickMeeting `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clickMeeting/latest/actions/list-chats?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clickMeeting/latest/actions/list-chats?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "date": "2026-05-07T12:00:00.000Z",
      "download_link": "https://example.com",
      "id": 1,
      "name": "Ava Chen",
      "time": "string",
      "timezone": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `date` | date | Chat archive date. |
| `download_link` | string | Chat archive download URL. |
| `id` | number | Chat archive identifier. |
| `name` | string | Conference name. |
| `time` | string | Chat archive time. |
| `timezone` | string | Archive time zone. |

## Native endpoint

Through the native ClickMeeting API, this operation is `GET chats` (base URL `https://api.clickmeeting.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-chats.md) for the provider-specific parameters and requirements.

