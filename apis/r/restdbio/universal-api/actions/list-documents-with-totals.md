# Restdb.io: List Documents With Totals

Retrieves documents and totals from a Restdb.io collection.

```
GET https://connect.mindcloud.co/v1/universal/restdbio/latest/actions/list-documents-with-totals
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Restdb.io `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/restdbio/latest/actions/list-documents-with-totals?connectionId=$CONNECTION_ID&limit=25&offset=0&collection=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "collection": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/restdbio/latest/actions/list-documents-with-totals?${params}`, {
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
| `collection` | string | yes | Collection name in the target Restdb.io database. |
| `q` | string | no | JSON query string to filter documents before totals are calculated. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Restdb.io API returns.

## Native endpoint

Through the native Restdb.io API, this operation is `GET /rest/:collection` (base URL `https://mindcloudstage0-7934.restdb.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-documents-with-totals.md) for the provider-specific parameters and requirements.

