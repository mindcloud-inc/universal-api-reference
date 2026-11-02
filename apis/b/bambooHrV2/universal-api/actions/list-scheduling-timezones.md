# BambooHR: List Scheduling Timezones

Lists scheduling timezones from BambooHR.

```
GET https://connect.mindcloud.co/v1/universal/bambooHrV2/latest/actions/list-scheduling-timezones
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BambooHR `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bambooHrV2/latest/actions/list-scheduling-timezones?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bambooHrV2/latest/actions/list-scheduling-timezones?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `filter` | string | no | OData filter expression applied to the `name` field. Supported operators: `eq` (exact match), `ne` (exclude), `and` (combine clauses). Supported string functions: `contains`, `startswith`, `endswith` (all case-insensitive). Not supported: `or`, `not`, parenthesized grouping. Examples: `name eq 'America/Denver'`, `name ne 'UTC'`, `contains(name, 'America')`, `startswith(name, 'US/')`, `endswith(name, 'York')`. |
| `sort` | string | no | Sorting options. Supported sort fields: `name` (alphabetical), `offset` (numeric UTC offset). Example: `name asc` or `offset desc` |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native BambooHR API returns.

## Native endpoint

Through the native BambooHR API, this operation is `GET /v1/scheduling/timezones` (base URL `https://{{credentials.companyDomain}}.bamboohr.com/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-scheduling-timezones.md) for the provider-specific parameters and requirements.

