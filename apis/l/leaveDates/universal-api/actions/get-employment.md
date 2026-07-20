# Leave Dates: Get Employment

Retrieves employment details from Leave Dates.

```
GET https://connect.mindcloud.co/v1/universal/leaveDates/latest/actions/get-employment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Leave Dates `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/leaveDates/latest/actions/get-employment?connectionId=$CONNECTION_ID&id=string&company=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string",
  "company": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/leaveDates/latest/actions/get-employment?${params}`, {
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
| `id` | string | yes |  |
| `company` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "allowances": [
        {}
      ],
      "company": {},
      "company_id": "string",
      "created_at": "string",
      "department": {},
      "department_id": "string",
      "email": "ava@example.com",
      "full_name": "Ava Chen",
      "holiday_location": "string",
      "id": "string",
      "is_admin": true,
      "is_approver": true,
      "status": "string",
      "timezone": "string",
      "updated_at": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allowances` | array<object> |  |
| `company` | object |  |
| `company_id` | string |  |
| `created_at` | string |  |
| `department` | object |  |
| `department_id` | string |  |
| `email` | string |  |
| `full_name` | string |  |
| `holiday_location` | string |  |
| `id` | string |  |
| `is_admin` | boolean |  |
| `is_approver` | boolean |  |
| `status` | string |  |
| `timezone` | string |  |
| `updated_at` | string |  |

## Native endpoint

Through the native Leave Dates API, this operation is `GET /employments/:id` (base URL `https://api.leavedates.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-employment.md) for the provider-specific parameters and requirements.

