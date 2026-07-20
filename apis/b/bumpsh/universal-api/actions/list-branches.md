# Bump.sh: List Branches

Retrieves branches from a Bump.sh documentation.

```
GET https://connect.mindcloud.co/v1/universal/bumpsh/latest/actions/list-branches
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bump.sh `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bumpsh/latest/actions/list-branches?connectionId=$CONNECTION_ID&doc_id_or_slug=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "doc_id_or_slug": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bumpsh/latest/actions/list-branches?${params}`, {
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
| `doc_id_or_slug` | string | yes | Documentation ID or slug. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Bump.sh API returns.

## Native endpoint

Through the native Bump.sh API, this operation is `GET docs/:doc_id_or_slug/branches` (base URL `https://bump.sh/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-branches.md) for the provider-specific parameters and requirements.

