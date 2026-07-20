# ClickMeeting: List Access Tokens

Retrieves access tokens for a conference in ClickMeeting.

```
GET https://connect.mindcloud.co/v1/universal/clickMeeting/latest/actions/list-access-tokens
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ClickMeeting `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clickMeeting/latest/actions/list-access-tokens?connectionId=$CONNECTION_ID&room_id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "room_id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clickMeeting/latest/actions/list-access-tokens?${params}`, {
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
      "access_tokens": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `access_tokens` | array<object> | Access tokens assigned to the room. |

## Native endpoint

Through the native ClickMeeting API, this operation is `GET conferences/{{room_id}}/tokens` (base URL `https://api.clickmeeting.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-access-tokens.md) for the provider-specific parameters and requirements.

