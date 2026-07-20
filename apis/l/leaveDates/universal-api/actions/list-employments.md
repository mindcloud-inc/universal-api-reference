# Leave Dates: List Employments

Retrieves employment records for a company in Leave Dates.

```
GET https://connect.mindcloud.co/v1/universal/leaveDates/latest/actions/list-employments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Leave Dates `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/leaveDates/latest/actions/list-employments?connectionId=$CONNECTION_ID&company=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "company": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/leaveDates/latest/actions/list-employments?${params}`, {
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
| `company` | string | yes |  |
| `departmentId` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "company_id": "string",
      "created_at": "string",
      "deleted_at": "string",
      "department": {},
      "email": "ava@example.com",
      "full_name": "Ava Chen",
      "holiday_location": "string",
      "id": "string",
      "is_admin": true,
      "is_approver": true,
      "status": "string",
      "timezone": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `company_id` | string |  |
| `created_at` | string |  |
| `deleted_at` | string |  |
| `department` | object |  |
| `email` | string |  |
| `full_name` | string |  |
| `holiday_location` | string |  |
| `id` | string |  |
| `is_admin` | boolean |  |
| `is_approver` | boolean |  |
| `status` | string |  |
| `timezone` | string |  |

## Native endpoint

Through the native Leave Dates API, this operation is `GET /employments` (base URL `https://api.leavedates.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-employments.md) for the provider-specific parameters and requirements.

