# Project Bubble: Get User

Retrieves a Project Bubble user by ID.

```
GET https://connect.mindcloud.co/v1/universal/projectBubble/latest/actions/get-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Project Bubble `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/projectBubble/latest/actions/get-user?connectionId=$CONNECTION_ID&user_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "user_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/projectBubble/latest/actions/get-user?${params}`, {
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
| `user_id` | string | yes | The Project Bubble user ID to fetch. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Project Bubble API returns.

## Native endpoint

Through the native Project Bubble API, this operation is `GET /users/:user_id` (base URL `https://api.projectbubble.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user.md) for the provider-specific parameters and requirements.

