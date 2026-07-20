# Ninety.io: Query Measurables

Retrieves measurables from Ninety.io with optional filters.

```
GET https://connect.mindcloud.co/v1/universal/ninetyio/latest/actions/query-measurables
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ninety.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ninetyio/latest/actions/query-measurables?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ninetyio/latest/actions/query-measurables?${params}`, {
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
| `excludeKpiIds[]` | array<string> | no | Array of Measurable Ids to exclude from the response |
| `pageIndex` | number | no | The page number to retrieve |
| `pageSize` | number | no | The number of items to retrieve per page |
| `periodInterval` | string | no | Limits results to Measurables with the specified period interval |
| `searchOwner` | string | no | The name of the owner of the Measurables to retrieve |
| `searchText` | string | no | Text to search for in the Measurable title or description |
| `searchTitle` | string | no | Text to search for in the Measurable title only |
| `sortField` | string | no | The field to sort Measurables by |
| `sortDirection` | string | no | The sort direction for the selected sort field |
| `unassignedOnly` | boolean | no | Only include Measurables that have no owner assigned |
| `userIds[]` | array<string> | no | An array of user Ids to filter Measurables by owner |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Ninety.io API returns.

## Native endpoint

Through the native Ninety.io API, this operation is `POST /v1/scorecard/kpis/query` (base URL `https://api.public.ninety.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/query-measurables.md) for the provider-specific parameters and requirements.

