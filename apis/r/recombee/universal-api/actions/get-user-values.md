# Recombee: Get User Values

Retrieves values for a user from Recombee.

```
GET https://connect.mindcloud.co/v1/universal/recombee/latest/actions/get-user-values
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Recombee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/recombee/latest/actions/get-user-values?connectionId=$CONNECTION_ID&userId=user-123" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "userId": "user-123"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/recombee/latest/actions/get-user-values?${params}`, {
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
| `userId` | string | yes | Example: `user-123`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Recombee API returns.

## Native endpoint

Through the native Recombee API, this operation is `GET /users/:userId` (base URL `https://rapi.recombee.com/{{credentials.databaseId}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-values.md) for the provider-specific parameters and requirements.

