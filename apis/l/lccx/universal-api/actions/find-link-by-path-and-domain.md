# lc.cx: Find Link By Path And Domain

Finds a short link in lc.cx by path and domain.

```
GET https://connect.mindcloud.co/v1/universal/lccx/latest/actions/find-link-by-path-and-domain
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a lc.cx `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lccx/latest/actions/find-link-by-path-and-domain?connectionId=$CONNECTION_ID&path=string&domainId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "path": "string",
  "domainId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lccx/latest/actions/find-link-by-path-and-domain?${params}`, {
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
| `path` | string | yes | The shortlink path to look up. |
| `domainId` | string | yes | The domain ID that owns the requested path. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native lc.cx API returns.

## Native endpoint

Through the native lc.cx API, this operation is `GET /links` (base URL `https://api.lc.cx/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/find-link-by-path-and-domain.md) for the provider-specific parameters and requirements.

