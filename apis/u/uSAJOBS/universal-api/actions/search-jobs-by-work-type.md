# USAJOBS: Search Jobs By Work Type

Finds jobs in USAJOBS by work type.

```
GET https://connect.mindcloud.co/v1/universal/uSAJOBS/latest/actions/search-jobs-by-work-type
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a USAJOBS `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uSAJOBS/latest/actions/search-jobs-by-work-type?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/uSAJOBS/latest/actions/search-jobs-by-work-type?${params}`, {
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
| `positionOfferingTypeCode` | string | no | Position offering/work type code. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native USAJOBS API returns.

## Native endpoint

Through the native USAJOBS API, this operation is `GET /api/Search` (base URL `https://data.usajobs.gov`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-jobs-by-work-type.md) for the provider-specific parameters and requirements.

