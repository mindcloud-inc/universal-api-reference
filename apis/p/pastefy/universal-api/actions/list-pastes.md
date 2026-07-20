# Pastefy: List Pastes



```
GET https://connect.mindcloud.co/v1/universal/pastefy/latest/actions/list-pastes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pastefy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pastefy/latest/actions/list-pastes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pastefy/latest/actions/list-pastes?${params}`, {
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
| `filterTags` | string | no |  |
| `page` | number | no |  |
| `pageLimit` | number | no |  |
| `userId` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Pastefy API returns.

## Native endpoint

Through the native Pastefy API, this operation is `GET /paste` (base URL `https://pastefy.app/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-pastes.md) for the provider-specific parameters and requirements.

