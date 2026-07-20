# TimeRex: Get User Primary Team

Retrieves the current user's primary team from TimeRex.

```
GET https://connect.mindcloud.co/v1/universal/timeRex/latest/actions/get-user-primary-team
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TimeRex `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timeRex/latest/actions/get-user-primary-team?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timeRex/latest/actions/get-user-primary-team?${params}`, {
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
      "id": "string",
      "isPrimary": true,
      "name": "Ava Chen",
      "role": "string",
      "urlPath": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `isPrimary` | boolean |  |
| `name` | string |  |
| `role` | string |  |
| `urlPath` | string |  |

## Native endpoint

Through the native TimeRex API, this operation is `GET /user/me/teams/primary` (base URL `https://timerex.net/api/beta`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-primary-team.md) for the provider-specific parameters and requirements.

