# Harpoon: List Expenses

Retrieves expenses from Harpoon.

```
GET https://connect.mindcloud.co/v1/universal/harpoon/latest/actions/list-expenses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Harpoon `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/harpoon/latest/actions/list-expenses?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/harpoon/latest/actions/list-expenses?${params}`, {
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
| `startDate` | date | no |  |
| `endDate` | date | no |  |
| `clients[]` | array<number> | no |  |
| `projects[]` | array<number> | no |  |
| `categories[]` | array<number> | no |  |
| `status` | string | no |  |
| `search` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "category": {},
      "category_id": "string",
      "client": {},
      "client_id": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "date": "2026-05-07T12:00:00.000Z",
      "date_formatted": "string",
      "description": "string",
      "id": "string",
      "project": {},
      "project_id": "string",
      "status": "string",
      "team_id": "string",
      "vendor": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number |  |
| `category` | object |  |
| `category_id` | string |  |
| `client` | object |  |
| `client_id` | string |  |
| `created_at` | date |  |
| `date` | date |  |
| `date_formatted` | string |  |
| `description` | string |  |
| `id` | string |  |
| `project` | object |  |
| `project_id` | string |  |
| `status` | string |  |
| `team_id` | string |  |
| `vendor` | string |  |

## Native endpoint

Through the native Harpoon API, this operation is `GET /expenses` (base URL `https://app.harpoonapp.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-expenses.md) for the provider-specific parameters and requirements.

