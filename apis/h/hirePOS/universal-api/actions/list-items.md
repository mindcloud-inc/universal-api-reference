# HirePOS: List Items

Finds items in HirePOS by item search fields.

```
GET https://connect.mindcloud.co/v1/universal/hirePOS/latest/actions/list-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HirePOS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hirePOS/latest/actions/list-items?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hirePOS/latest/actions/list-items?${params}`, {
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
| `code` | string | no | Find an item by its HirePOS item code. |
| `barcode` | string | no | Find an item by barcode. |
| `supplierCode` | string | no | Find an item by supplier code. |
| `serial` | string | no | Find an item by serial tracking number. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native HirePOS API returns.

## Native endpoint

Through the native HirePOS API, this operation is `GET /Items` (base URL `https://api.hirepos.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-items.md) for the provider-specific parameters and requirements.

