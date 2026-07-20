# Teyuto: Delete Session

Deletes an existing authenticated Teyuto session.

```
DELETE https://connect.mindcloud.co/v1/universal/teyuto/latest/actions/delete-session
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Teyuto `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/teyuto/latest/actions/delete-session?connectionId=$CONNECTION_ID&userId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "userId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/teyuto/latest/actions/delete-session?${params}`, {
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
| `userId` | string | yes | User ID whose session should be revoked. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Teyuto API returns.

## Native endpoint

Through the native Teyuto API, this operation is `DELETE /sessions` (base URL `https://api.teyuto.tv/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-session.md) for the provider-specific parameters and requirements.

