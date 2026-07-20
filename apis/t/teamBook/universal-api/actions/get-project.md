# TeamBook: Get Project

Retrieves detailed project information from TeamBook.

```
GET https://connect.mindcloud.co/v1/universal/teamBook/latest/actions/get-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TeamBook `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/teamBook/latest/actions/get-project?connectionId=$CONNECTION_ID&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/teamBook/latest/actions/get-project?${params}`, {
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
| `projectId` | string | yes | The TeamBook project identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": "string",
      "booked_duration": "string",
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
| `booked_duration` | string |  |
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

Through the native TeamBook API, this operation is `GET /projects/{projectId}` (base URL `https://web.teambookapp.com/api/public`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project.md) for the provider-specific parameters and requirements.

