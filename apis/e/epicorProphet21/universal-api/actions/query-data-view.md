# Epicor Prophet 21: Query Data View



```
GET https://connect.mindcloud.co/v1/universal/epicorProphet21/latest/actions/query-data-view
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Epicor Prophet 21 `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/epicorProphet21/latest/actions/query-data-view?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/epicorProphet21/latest/actions/query-data-view?${params}`, {
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
| `view` | string | no | The Prophet 21 data view name, such as p21_view_customer. Default: `invoice_hdr`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `select` | string | no | Comma-separated field names. Leave empty to return all available fields. |
| `filter` | string | no | A Prophet 21 filter expression, such as customer_id eq 123. |
| `count` | boolean | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Epicor Prophet 21 API returns.

## Native endpoint

Through the native Epicor Prophet 21 API, this operation is `GET /data/erp/views/v1/:view` (base URL `{{credentials.apiUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/query-data-view.md) for the provider-specific parameters and requirements.

