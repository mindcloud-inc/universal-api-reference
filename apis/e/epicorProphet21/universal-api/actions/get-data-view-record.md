# Epicor Prophet 21: Get Data View Record



```
GET https://connect.mindcloud.co/v1/universal/epicorProphet21/latest/actions/get-data-view-record
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Epicor Prophet 21 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/epicorProphet21/latest/actions/get-data-view-record?connectionId=$CONNECTION_ID&view=p21_view_oe_hdr&key='1001234'" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "view": "p21_view_oe_hdr",
  "key": "'1001234'"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/epicorProphet21/latest/actions/get-data-view-record?${params}`, {
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
| `view` | list<string> | yes | Example: `p21_view_oe_hdr`. |
| `key` | string | yes | OData key expression, including quotes for string keys. For compound keys, name each part and preserve its documented type. Example: `'1001234'`. |
| `select` | string | no | Accepts multiple values in one string, delimited by `,`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Epicor Prophet 21 API returns.

## Native endpoint

Through the native Epicor Prophet 21 API, this operation is `GET /data/erp/views/v1/:view(:key)` (base URL `{{credentials.apiUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-data-view-record.md) for the provider-specific parameters and requirements.

