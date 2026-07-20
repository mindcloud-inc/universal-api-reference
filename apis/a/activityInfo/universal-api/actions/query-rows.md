# ActivityInfo: Query Rows

Queries rows from ActivityInfo form data.

```
GET https://connect.mindcloud.co/v1/universal/activityInfo/latest/actions/query-rows
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ActivityInfo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/activityInfo/latest/actions/query-rows?connectionId=$CONNECTION_ID&rowSources%5B%5D=%5Bobject%20Object%5D&columns%5B%5D=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "rowSources[]": "[object Object]",
  "columns[]": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/activityInfo/latest/actions/query-rows?${params}`, {
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
| `rowSources[]` | array<object> | yes | Forms to query as row sources. |
| `columns[]` | array<object> | yes | Columns to return. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ActivityInfo API returns.

## Native endpoint

Through the native ActivityInfo API, this operation is `POST /resources/query/rows` (base URL `https://www.activityinfo.org`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/query-rows.md) for the provider-specific parameters and requirements.

