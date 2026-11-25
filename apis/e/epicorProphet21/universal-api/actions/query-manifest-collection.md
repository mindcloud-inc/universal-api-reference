# Epicor Prophet 21: Query Manifest Collection



```
GET https://connect.mindcloud.co/v1/universal/epicorProphet21/latest/actions/query-manifest-collection
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Epicor Prophet 21 `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/epicorProphet21/latest/actions/query-manifest-collection?connectionId=$CONNECTION_ID&limit=25&offset=0&collection=clippership_return_10004" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "collection": "clippership_return_10004"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/epicorProphet21/latest/actions/query-manifest-collection?${params}`, {
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
| `collection` | list<string> | yes | Example: `clippership_return_10004`. |
| `select` | string | no | Accepts multiple values in one string, delimited by `,`. Example: `supplier_id,supplier_name`. |
| `filter` | string | no | OData filter expression. Quote string values and double embedded single quotes. Combine values with or; do not use in, which can be silently ignored. Example: `supplier_id eq 10050`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `inlinecount` | list<string> | no | One of: `allpages`, `none`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Epicor Prophet 21 API returns.

## Native endpoint

Through the native Epicor Prophet 21 API, this operation is `GET /data/manifest/v1/:collection` (base URL `{{credentials.apiUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/query-manifest-collection.md) for the provider-specific parameters and requirements.

