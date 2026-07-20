# Basin: List Submissions

Retrieves submission records from Basin.

```
GET https://connect.mindcloud.co/v1/universal/basin/latest/actions/list-submissions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Basin `connectionId` ([setup](../authentication.md)).

This action also supports [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/basin/latest/actions/list-submissions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/basin/latest/actions/list-submissions?${params}`, {
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
| `formId` | string | no | Retrieve submissions for a specific Basin form. Optional when using a Form API key. |
| `filterBy` | string | no | Filter submissions by new, spam, trash, or all. |
| `query` | string | no | Search submissions by query. |
| `orderBy` | string | no | Order submissions by date_asc, date_desc, email_asc, or email_desc. |
| `dateRange` | string | no | Filter submissions by date range in the format YYYY-MM-DD+to+YYYY-MM-DD. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Basin API returns.

## Native endpoint

Through the native Basin API, this operation is `GET /api/v1/submissions` (base URL `https://usebasin.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-submissions.md) for the provider-specific parameters and requirements.

