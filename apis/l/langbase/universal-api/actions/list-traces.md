# Langbase: List Traces



```
GET https://connect.mindcloud.co/v1/universal/langbase/latest/actions/list-traces
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Langbase `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/langbase/latest/actions/list-traces?connectionId=$CONNECTION_ID&primitiveId=string&primitiveName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "primitiveId": "string",
  "primitiveName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/langbase/latest/actions/list-traces?${params}`, {
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
| `primitiveId` | string | yes | Primitive ID to filter traces by. |
| `primitiveName` | string | yes | Primitive name to filter traces by. |
| `limit` | number | no | Maximum number of traces to return. |
| `offset` | number | no | Number of traces to skip. |
| `order` | list | no | Sort order for traces. One of: `0`, `1`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Langbase API returns.

## Native endpoint

Through the native Langbase API, this operation is `GET v1/traces` (base URL `https://api.langbase.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-traces.md) for the provider-specific parameters and requirements.

