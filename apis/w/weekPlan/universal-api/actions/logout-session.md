# Week Plan: Logout Session



```
DELETE https://connect.mindcloud.co/v1/universal/weekPlan/latest/actions/logout-session
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Week Plan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/weekPlan/latest/actions/logout-session?connectionId=$CONNECTION_ID&refreshToken=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "refreshToken": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/weekPlan/latest/actions/logout-session?${params}`, {
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
| `refreshToken` | string | yes | Week Plan refresh token to invalidate during logout. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Message": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Message` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Week Plan API, this operation is `POST https://backend-api.weekplan.net/sessions/logout` (base URL `https://api.weekplan.net/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/logout-session.md) for the provider-specific parameters and requirements.

