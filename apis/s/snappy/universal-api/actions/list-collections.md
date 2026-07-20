# Snappy: List Collections

Retrieves collections from Snappy.

```
GET https://connect.mindcloud.co/v1/universal/snappy/latest/actions/list-collections
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Snappy `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/snappy/latest/actions/list-collections?connectionId=$CONNECTION_ID&limit=25&offset=0&budget=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "budget": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/snappy/latest/actions/list-collections?${params}`, {
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
| `budget` | number | yes | Budget value. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `companyId` | string | no | Company ID. |
| `accountId` | string | no | Account ID. |
| `countries[]` | array<string> | no | List of supported countries. Default: `["US"]`. |
| `types[]` | array<string> | no | List of collection types. |
| `fields[]` | array<string> | no | Additional collection fields to include. |
| `skip` | number | no | Number of records to skip for pagination. |
| `limit` | number | no | Maximum number of records to return per page. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Snappy API returns.

## Native endpoint

Through the native Snappy API, this operation is `GET /collections` (base URL `https://api.snappy.com/public-api/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-collections.md) for the provider-specific parameters and requirements.

