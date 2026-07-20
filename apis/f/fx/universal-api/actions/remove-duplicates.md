# 1001fx: Remove Duplicates

Removes duplicate items from an array.

```
GET https://connect.mindcloud.co/v1/universal/fx/latest/actions/remove-duplicates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 1001fx `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fx/latest/actions/remove-duplicates?connectionId=$CONNECTION_ID&data%5B%5D=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "data[]": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fx/latest/actions/remove-duplicates?${params}`, {
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
| `data[]` | array | yes | Array of objects to deduplicate. |
| `fields[]` | array | no | Fields used to determine duplicate rows. |
| `ignoreCase` | boolean | no | Whether string comparison should ignore case. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native 1001fx API returns.

## Native endpoint

Through the native 1001fx API, this operation is `POST /array/removeduplicates` (base URL `https://api.1001fx.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-duplicates.md) for the provider-specific parameters and requirements.

