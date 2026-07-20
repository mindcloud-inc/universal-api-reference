# Bump.sh: Create Diff

Creates a diff in Bump.sh.

```
POST https://connect.mindcloud.co/v1/universal/bumpsh/latest/actions/create-diff
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bump.sh `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bumpsh/latest/actions/create-diff" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "definition": "string",
  "previous_definition": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bumpsh/latest/actions/create-diff', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "definition": "string",
    "previous_definition": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `definition` | string | yes | Serialized current OpenAPI or AsyncAPI definition. |
| `previous_definition` | string | yes | Serialized previous OpenAPI or AsyncAPI definition. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Bump.sh API returns.

## Native endpoint

Through the native Bump.sh API, this operation is `POST diffs` (base URL `https://bump.sh/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-diff.md) for the provider-specific parameters and requirements.

