# Pastebin: List My Pastes

Retrieves pastes created by the current Pastebin user.

```
GET https://connect.mindcloud.co/v1/universal/pastebin/latest/actions/list-my-pastes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pastebin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pastebin/latest/actions/list-my-pastes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pastebin/latest/actions/list-my-pastes?${params}`, {
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
| `resultsLimit` | string | no | Optional number of pastes to return. Pastebin defaults to 50 and allows up to 1000. Default: `50`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Pastebin API returns.

## Native endpoint

Through the native Pastebin API, this operation is `POST /api_post.php` (base URL `https://pastebin.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-my-pastes.md) for the provider-specific parameters and requirements.

