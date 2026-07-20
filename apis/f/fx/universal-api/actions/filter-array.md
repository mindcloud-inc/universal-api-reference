# 1001fx: Filter Array

Filters an array by a comparison operator.

```
GET https://connect.mindcloud.co/v1/universal/fx/latest/actions/filter-array
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 1001fx `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fx/latest/actions/filter-array?connectionId=$CONNECTION_ID&criteria=string&data%5B%5D=string&queryField=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "criteria": "string",
  "data[]": "string",
  "queryField": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fx/latest/actions/filter-array?${params}`, {
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
| `criteria` | string | yes | Value to compare against when filtering. |
| `data[]` | array | yes | Array of objects to filter. |
| `ignoreCase` | boolean | no | Whether string filtering should ignore case. |
| `operator` | string | no | Operator used for the filter comparison. |
| `queryField` | string | yes | Field name to evaluate in each array item. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native 1001fx API returns.

## Native endpoint

Through the native 1001fx API, this operation is `POST /array/filterarray` (base URL `https://api.1001fx.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/filter-array.md) for the provider-specific parameters and requirements.

