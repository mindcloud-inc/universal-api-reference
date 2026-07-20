# Rossum: Validate Schema

Validates a schema in Rossum.

```
GET https://connect.mindcloud.co/v1/universal/rossum/latest/actions/validate-schema
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rossum `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rossum/latest/actions/validate-schema?connectionId=$CONNECTION_ID&content=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "content": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rossum/latest/actions/validate-schema?${params}`, {
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
| `content` | list<object> | yes | Rossum schema content definition. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Rossum API returns.

## Native endpoint

Through the native Rossum API, this operation is `POST /schemas/validate` (base URL `https://mindcloud.rossum.app/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-schema.md) for the provider-specific parameters and requirements.

