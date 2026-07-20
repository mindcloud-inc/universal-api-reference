# Harpoon: List Estimates

Retrieves estimates from Harpoon.

```
GET https://connect.mindcloud.co/v1/universal/harpoon/latest/actions/list-estimates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Harpoon `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/harpoon/latest/actions/list-estimates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/harpoon/latest/actions/list-estimates?${params}`, {
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
| `year` | number | no |  |
| `clients[]` | array<number> | no |  |
| `projects[]` | array<number> | no |  |
| `status` | string | no |  |
| `search` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": "string",
      "client_id": 1,
      "company_name": "Ava Chen",
      "created_at": "2026-05-07T12:00:00.000Z",
      "document_id": "string",
      "email": "ava@example.com",
      "id": 1,
      "issue_date": "2026-05-07T12:00:00.000Z",
      "note": "string",
      "phone": "string",
      "project_id": 1,
      "status": "string",
      "subject": "string",
      "total": 1,
      "uuid": "string",
      "valid_until": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string |  |
| `client_id` | number |  |
| `company_name` | string |  |
| `created_at` | date |  |
| `document_id` | string |  |
| `email` | string |  |
| `id` | number |  |
| `issue_date` | date |  |
| `note` | string |  |
| `phone` | string |  |
| `project_id` | number |  |
| `status` | string |  |
| `subject` | string |  |
| `total` | number |  |
| `uuid` | string |  |
| `valid_until` | date |  |

## Native endpoint

Through the native Harpoon API, this operation is `GET /estimates` (base URL `https://app.harpoonapp.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-estimates.md) for the provider-specific parameters and requirements.

