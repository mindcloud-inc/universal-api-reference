# Leave Dates: Add Department

Creates a new department in Leave Dates.

```
POST https://connect.mindcloud.co/v1/universal/leaveDates/latest/actions/add-department
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Leave Dates `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/leaveDates/latest/actions/add-department" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "companyId": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/leaveDates/latest/actions/add-department', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "companyId": "string",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `companyId` | string | yes |  |
| `name` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "company_id": "string",
      "created_at": "string",
      "id": "string",
      "is_enabled_to_see_employment_own_data": true,
      "name": "Ava Chen",
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
| `id` | string |  |
| `is_enabled_to_see_employment_own_data` | boolean |  |
| `name` | string |  |
| `updated_at` | string |  |

## Native endpoint

Through the native Leave Dates API, this operation is `POST /departments` (base URL `https://api.leavedates.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-department.md) for the provider-specific parameters and requirements.

