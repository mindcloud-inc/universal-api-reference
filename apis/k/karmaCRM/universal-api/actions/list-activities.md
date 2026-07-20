# Karma CRM: List Activities

Retrieves a list of activities from Karma CRM.

```
GET https://connect.mindcloud.co/v1/universal/karmaCRM/latest/actions/list-activities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Karma CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/karmaCRM/latest/actions/list-activities?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/karmaCRM/latest/actions/list-activities?${params}`, {
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
| `page` | number | no | Page number to retrieve. |
| `perPage` | number | no | Number of activities per page. |
| `dueCategory` | string | no | Filter based on due_at date, for example overdue or today. |
| `todoCategoryId[]` | array<number> | no | Filter based on todo category IDs. |
| `userFilter` | string | no | Filter by mine or a specific user ID. |
| `dueAtSort` | string | no | Sort due_at ascending asc or descending desc. |
| `columns[]` | array<string> | no | Columns to include in results, for example body or due_at. Accepts multiple values as an array. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Karma CRM API returns.

## Native endpoint

Through the native Karma CRM API, this operation is `GET /api/v3/activities.json` (base URL `https://app.karmacrm.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-activities.md) for the provider-specific parameters and requirements.

