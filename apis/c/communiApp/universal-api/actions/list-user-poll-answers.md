# Communi App: List User Poll Answers



```
GET https://connect.mindcloud.co/v1/universal/communiApp/latest/actions/list-user-poll-answers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Communi App `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/communiApp/latest/actions/list-user-poll-answers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/communiApp/latest/actions/list-user-poll-answers?${params}`, {
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
| `poll` | number | no |  |
| `user` | number | no |  |
| `answerId` | number | no |  |
| `isSelected` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_loadStatus": 1,
      "_rls": 1,
      "createdOn": "string",
      "id": "string",
      "poll": 1,
      "pollAnswer": 1,
      "updatedOn": "string",
      "user": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_loadStatus` | number |  |
| `_rls` | number |  |
| `createdOn` | string |  |
| `id` | string |  |
| `poll` | number |  |
| `pollAnswer` | number |  |
| `updatedOn` | string |  |
| `user` | number |  |

## Native endpoint

Through the native Communi App API, this operation is `GET /rest/userPollAnswer` (base URL `https://api.communiapp.de`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-user-poll-answers.md) for the provider-specific parameters and requirements.

