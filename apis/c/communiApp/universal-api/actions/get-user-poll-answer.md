# Communi App: Get User Poll Answer



```
GET https://connect.mindcloud.co/v1/universal/communiApp/latest/actions/get-user-poll-answer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Communi App `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/communiApp/latest/actions/get-user-poll-answer?connectionId=$CONNECTION_ID&id=343753-1-0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "343753-1-0"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/communiApp/latest/actions/get-user-poll-answer?${params}`, {
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
| `id` | string | yes | Default: `343753-1-0`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "answerId": 1,
      "id": "string",
      "isSelected": true,
      "poll": 1,
      "user": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `answerId` | number |  |
| `id` | string |  |
| `isSelected` | boolean |  |
| `poll` | number |  |
| `user` | number |  |

## Native endpoint

Through the native Communi App API, this operation is `GET /rest/userPollAnswer/:id` (base URL `https://api.communiapp.de`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-poll-answer.md) for the provider-specific parameters and requirements.

