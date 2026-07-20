# TeamBook: List Projects

Retrieves all project records from TeamBook.

```
GET https://connect.mindcloud.co/v1/universal/teamBook/latest/actions/list-projects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TeamBook `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/teamBook/latest/actions/list-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/teamBook/latest/actions/list-projects?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "active": "string",
      "business_unit": "string",
      "client_id": "string",
      "code": "string",
      "color": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "custom_fields": [
        [
          "string"
        ]
      ],
      "end_date": "2026-05-07T12:00:00.000Z",
      "estimated": "string",
      "id": "string",
      "kind": "string",
      "manager": {
        "email": "ava@example.com",
        "id": 1,
        "name": "Ava Chen"
      },
      "name": "Ava Chen",
      "notes": "string",
      "start_date": "2026-05-07T12:00:00.000Z",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | string |  |
| `business_unit` | string |  |
| `client_id` | string |  |
| `code` | string |  |
| `color` | string |  |
| `created_at` | date |  |
| `custom_fields[]` | array<string> |  |
| `end_date` | date |  |
| `estimated` | string |  |
| `id` | string |  |
| `kind` | string |  |
| `manager.email` | string |  |
| `manager.id` | number |  |
| `manager.name` | string |  |
| `name` | string |  |
| `notes` | string |  |
| `start_date` | date |  |
| `updated_at` | date |  |

## Native endpoint

Through the native TeamBook API, this operation is `GET /projects` (base URL `https://web.teambookapp.com/api/public`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-projects.md) for the provider-specific parameters and requirements.

