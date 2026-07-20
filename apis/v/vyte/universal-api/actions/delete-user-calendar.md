# Vyte: Delete User Calendar

Deletes a user's calendar from Vyte.

```
DELETE https://connect.mindcloud.co/v1/universal/vyte/latest/actions/delete-user-calendar
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vyte `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/vyte/latest/actions/delete-user-calendar?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vyte/latest/actions/delete-user-calendar?${params}`, {
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
| `calendarId` | string | no | The Vyte calendar ID. Default: `69cac1a8d31001784f0421c4`. |
| `userId` | string | no | The Vyte user ID. Default: `69ca9fead310017cb903a0fd`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Vyte API returns.

## Native endpoint

Through the native Vyte API, this operation is `DELETE v2/users/:user_id/calendars/:calendar_id` (base URL `https://api.vyte.in`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-user-calendar.md) for the provider-specific parameters and requirements.

