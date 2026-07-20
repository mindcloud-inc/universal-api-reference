# Baserow: List Row Names

Retrieves primary row names from Baserow.

```
GET https://connect.mindcloud.co/v1/universal/baserow/latest/actions/list-row-names
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Baserow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/baserow/latest/actions/list-row-names?connectionId=$CONNECTION_ID&tableId=1&rowIds%5B%5D=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "tableId": "1",
  "rowIds[]": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/baserow/latest/actions/list-row-names?${params}`, {
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
| `tableId` | number | yes | The table whose row names you want to fetch. |
| `rowIds[]` | array<number> | yes | The row IDs whose primary-field names you want to fetch. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Baserow API returns.

## Native endpoint

Through the native Baserow API, this operation is `GET /api/database/rows/names/` (base URL `https://api.baserow.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-row-names.md) for the provider-specific parameters and requirements.

