# Leave Dates: Add Employment

Creates a new employment in Leave Dates.

```
POST https://connect.mindcloud.co/v1/universal/leaveDates/latest/actions/add-employment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Leave Dates `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/leaveDates/latest/actions/add-employment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "companyId": "string",
  "fullName": "Ava Chen",
  "email": "ava@example.com",
  "timezone": "string",
  "holidayLocation": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/leaveDates/latest/actions/add-employment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
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
| `companyId` | string | yes | Company ID for the employment |
| `fullName` | string | yes | Full name of the employee |
| `email` | string | yes | Employee email address |
| `timezone` | string | yes | Employment timezone |
| `holidayLocation` | string | yes | Holiday location label |
| `isAdmin` | boolean | no | Whether the employment is an admin user Default: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "company_id": "string",
      "created_at": "string",
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
| `company_id` | string |  |
| `created_at` | string |  |
| `email` | string |  |
| `full_name` | string |  |
| `holiday_location` | string |  |
| `id` | string |  |
| `is_admin` | boolean |  |
| `is_approver` | boolean |  |
| `timezone` | string |  |
| `updated_at` | string |  |

## Native endpoint

Through the native Leave Dates API, this operation is `POST /employments` (base URL `https://api.leavedates.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-employment.md) for the provider-specific parameters and requirements.

