# Pastebin: Delete My Paste

Deletes a paste created by the current Pastebin user.

```
DELETE https://connect.mindcloud.co/v1/universal/pastebin/latest/actions/delete-my-paste
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pastebin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/pastebin/latest/actions/delete-my-paste?connectionId=$CONNECTION_ID&pasteKey=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "pasteKey": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pastebin/latest/actions/delete-my-paste?${params}`, {
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
| `pasteKey` | string | yes | Pastebin key for the member-owned paste to delete. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Pastebin API returns.

## Native endpoint

Through the native Pastebin API, this operation is `POST /api_post.php` (base URL `https://pastebin.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-my-paste.md) for the provider-specific parameters and requirements.

