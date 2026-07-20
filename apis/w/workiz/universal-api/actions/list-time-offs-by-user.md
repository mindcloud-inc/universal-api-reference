# Workiz: List Time Offs by User

Finds time off entries in Workiz by user name.

```
GET https://connect.mindcloud.co/v1/universal/workiz/latest/actions/list-time-offs-by-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Workiz `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/workiz/latest/actions/list-time-offs-by-user?connectionId=$CONNECTION_ID&userName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "userName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/workiz/latest/actions/list-time-offs-by-user?${params}`, {
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
| `userName` | string | yes | The user's name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "end": "string",
      "start": "string",
      "userName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `end` | string |  |
| `start` | string |  |
| `userName` | string |  |

## Native endpoint

Through the native Workiz API, this operation is `GET /TimeOff/get/:USER_NAME` (base URL `https://api.workiz.com/api/v1/{{credentials.apiKey}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-time-offs-by-user.md) for the provider-specific parameters and requirements.

