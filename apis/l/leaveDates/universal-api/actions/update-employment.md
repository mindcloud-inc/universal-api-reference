# Leave Dates: Update Employment

Updates an existing employment in Leave Dates.

```
PUT https://connect.mindcloud.co/v1/universal/leaveDates/latest/actions/update-employment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Leave Dates `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/leaveDates/latest/actions/update-employment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "companyId": "string",
  "fullName": "Ava Chen",
  "email": "ava@example.com",
  "timezone": "string",
  "holidayLocation": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/leaveDates/latest/actions/update-employment', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "companyId": "string",
    "fullName": "Ava Chen",
    "email": "ava@example.com",
    "timezone": "string",
    "holidayLocation": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes |  |
| `companyId` | string | yes |  |
| `fullName` | string | yes |  |
| `email` | string | yes |  |
| `timezone` | string | yes |  |
| `holidayLocation` | string | yes |  |
| `isAdmin` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "company": {},
      "company_id": "string",
      "created_at": "string",
      "department": {},
      "email": "ava@example.com",
      "full_name": "Ava Chen",
      "holiday_location": "string",
      "id": "string",
      "is_admin": true,
      "is_approver": true,
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
| `company` | object |  |
| `company_id` | string |  |
| `created_at` | string |  |
| `department` | object |  |
| `email` | string |  |
| `full_name` | string |  |
| `holiday_location` | string |  |
| `id` | string |  |
| `is_admin` | boolean |  |
| `is_approver` | boolean |  |
| `timezone` | string |  |
| `updated_at` | string |  |

## Native endpoint

Through the native Leave Dates API, this operation is `PUT /employments/:id` (base URL `https://api.leavedates.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-employment.md) for the provider-specific parameters and requirements.

