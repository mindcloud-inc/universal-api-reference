# FreeAgent: List Expenses

Retrieves a list of expenses from FreeAgent.

```
GET https://connect.mindcloud.co/v1/universal/freeAgent/latest/actions/list-expenses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FreeAgent `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/freeAgent/latest/actions/list-expenses?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/freeAgent/latest/actions/list-expenses?${params}`, {
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
| `updatedSince` | date | no | Only return expenses updated after this timestamp. |
| `view` | string | no | Filter the expense collection by FreeAgent view. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "category": "string",
      "contact_name": "Ava Chen",
      "created_at": "2026-05-07T12:00:00.000Z",
      "currency": "string",
      "dated_on": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "gross_value": "string",
      "native_gross_value": "string",
      "project": "string",
      "project_name": "Ava Chen",
      "updated_at": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com",
      "user": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `category` | string |  |
| `contact_name` | string |  |
| `created_at` | date |  |
| `currency` | string |  |
| `dated_on` | date |  |
| `description` | string |  |
| `gross_value` | string |  |
| `native_gross_value` | string |  |
| `project` | string |  |
| `project_name` | string |  |
| `updated_at` | date |  |
| `url` | string |  |
| `user` | string |  |

## Native endpoint

Through the native FreeAgent API, this operation is `GET /expenses` (base URL `https://api.freeagent.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-expenses.md) for the provider-specific parameters and requirements.

