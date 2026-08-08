# Monday: Get All SubItems Of Of an Item by Item's Column Value

Retrieves items and their subitems from a Monday board by column value.

```
GET https://connect.mindcloud.co/v1/universal/monday/latest/actions/get-all-sub-items-of-of-an-item-by-items-column-value
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Monday `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/monday/latest/actions/get-all-sub-items-of-of-an-item-by-items-column-value?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/monday/latest/actions/get-all-sub-items-of-of-an-item-by-items-column-value?${params}`, {
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
| `columnId` | string | no |  |
| `compareValue[]` | array<string> | no |  |
| `boardId` | number | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Monday API returns.

## Native endpoint

Through the native Monday API, this operation is `POST` (base URL `https://api.monday.com/v2/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-all-sub-items-of-of-an-item-by-items-column-value.md) for the provider-specific parameters and requirements.

