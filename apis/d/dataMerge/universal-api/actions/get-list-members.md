# DataMerge: Get List Members

Retrieves items from a specific DataMerge list.

```
GET https://connect.mindcloud.co/v1/universal/dataMerge/latest/actions/get-list-members
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DataMerge `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dataMerge/latest/actions/get-list-members?connectionId=$CONNECTION_ID&limit=25&offset=0&objectType=string&list=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "objectType": "string",
  "list": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dataMerge/latest/actions/get-list-members?${params}`, {
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
| `objectType` | string | yes | List object type. |
| `list` | string | yes | List slug. |
| `page` | number | no | Page number. |
| `pageSize` | number | no | Page size. |
| `sortBy` | string | no | Sort field. |
| `sortOrder` | string | no | Sort order. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native DataMerge API returns.

## Native endpoint

Through the native DataMerge API, this operation is `GET /v1/lists/:object_type/:list` (base URL `https://api.datamerge.ai`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-list-members.md) for the provider-specific parameters and requirements.

