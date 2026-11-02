# BambooHR: List Breaks for Break Policy

Lists breaks for break policy from BambooHR.

```
GET https://connect.mindcloud.co/v1/universal/bambooHrV2/latest/actions/list-breaks-for-break-policy
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BambooHR `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bambooHrV2/latest/actions/list-breaks-for-break-policy?connectionId=$CONNECTION_ID&limit=25&offset=0&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bambooHrV2/latest/actions/list-breaks-for-break-policy?${params}`, {
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
| `id` | string | yes | The break policy ID. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `filter` | string | no | OData filter expression applied to breaks within the policy. Supported operators: `eq` (equals, use `eq null` to match NULL), `ne` (not equals, use `ne null` to match NOT NULL), `lt` (less than), `le` (less than or equal), `gt` (greater than), `ge` (greater than or equal), `in` (value in list), `and` (combine clauses). Not supported: `or`, `not`, parenthesized grouping. Filterable fields: `id`, `name`, `paid`, `duration`, `availabilityType`, `availabilityMinHoursWorked`, `availabilityMaxHoursWorked`, `availabilityStartTime`, `availabilityEndTime`, `createdAt`, `updatedAt`, `deletedAt`. Examples: `name eq 'Lunch'`, `paid eq true`, `paid eq false and name ne 'Quick Break'`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native BambooHR API returns.

## Native endpoint

Through the native BambooHR API, this operation is `GET /v1/time-tracking/break-policies/:id/breaks` (base URL `https://{{credentials.companyDomain}}.bamboohr.com/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-breaks-for-break-policy.md) for the provider-specific parameters and requirements.

