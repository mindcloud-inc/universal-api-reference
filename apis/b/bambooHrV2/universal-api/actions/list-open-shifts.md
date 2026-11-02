# BambooHR: List Open Shifts

Lists open shifts from BambooHR.

```
GET https://connect.mindcloud.co/v1/universal/bambooHrV2/latest/actions/list-open-shifts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BambooHR `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bambooHrV2/latest/actions/list-open-shifts?connectionId=$CONNECTION_ID&limit=25&offset=0&filter=start%20ge%202026-01-01T00%3A00%3A00Z%20and%20start%20lt%202026-01-08T00%3A00%3A00Z" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "filter": "start ge 2026-01-01T00:00:00Z and start lt 2026-01-08T00:00:00Z"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bambooHrV2/latest/actions/list-open-shifts?${params}`, {
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
| `filter` | string | yes | OData v4 filter expression. Required: a date window on start or end, bounded below (ge, gt, eq) and above (le, lt, eq), at most 31 days wide. Allowed fields: id, scheduleId, name, start, end, claimsRequireApproval. Example: `start ge 2026-01-01T00:00:00Z and start lt 2026-01-08T00:00:00Z`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sort` | string | no | Sort expression on any filterable field (e.g. start desc). Defaults to start ascending. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native BambooHR API returns.

## Native endpoint

Through the native BambooHR API, this operation is `GET /v1/scheduling/open-shifts` (base URL `https://{{credentials.companyDomain}}.bamboohr.com/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-open-shifts.md) for the provider-specific parameters and requirements.

