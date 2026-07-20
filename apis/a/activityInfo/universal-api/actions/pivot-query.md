# ActivityInfo: Pivot Query

Retrieves pivot query results from ActivityInfo.

```
GET https://connect.mindcloud.co/v1/universal/activityInfo/latest/actions/pivot-query
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ActivityInfo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/activityInfo/latest/actions/pivot-query?connectionId=$CONNECTION_ID&sources=%5Bobject%20Object%5D&model=%5Bobject%20Object%5D&showHidden=true" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sources": "[object Object]",
  "model": "[object Object]",
  "showHidden": "true"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/activityInfo/latest/actions/pivot-query?${params}`, {
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
| `sources` | object | yes | Pivot data sources. |
| `model` | object | yes | Pivot analysis model. |
| `showHidden` | boolean | yes | Whether to include hidden fields. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ActivityInfo API returns.

## Native endpoint

Through the native ActivityInfo API, this operation is `POST /resources/query/pivot` (base URL `https://www.activityinfo.org`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/pivot-query.md) for the provider-specific parameters and requirements.

