# Leave Dates: Create Leave Type

Creates a new leave type in Leave Dates.

```
POST https://connect.mindcloud.co/v1/universal/leaveDates/latest/actions/create-leave-type
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Leave Dates `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/leaveDates/latest/actions/create-leave-type" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "companyId": "string",
  "allowanceTypeId": "string",
  "name": "Ava Chen",
  "displayCode": "string",
  "displayIcon": "string",
  "colour": "string",
  "approval": true,
  "isHoliday": true,
  "onlyAdmin": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/leaveDates/latest/actions/create-leave-type', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "companyId": "string",
    "allowanceTypeId": "string",
    "name": "Ava Chen",
    "displayCode": "string",
    "displayIcon": "string",
    "colour": "string",
    "approval": true,
    "isHoliday": true,
    "onlyAdmin": true
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `companyId` | string | yes |  |
| `allowanceTypeId` | string | yes |  |
| `name` | string | yes |  |
| `displayCode` | string | yes |  |
| `displayIcon` | string | yes |  |
| `colour` | string | yes |  |
| `approval` | boolean | yes |  |
| `isHoliday` | boolean | yes |  |
| `onlyAdmin` | boolean | yes |  |
| `description` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accounts_to_conflicts": true,
      "allowance_type_id": "string",
      "approval": true,
      "colour": "string",
      "company_id": "string",
      "created_at": "string",
      "description": "string",
      "display_icon": "string",
      "id": "string",
      "name": "Ava Chen",
      "only_admin": true,
      "updated_at": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accounts_to_conflicts` | boolean |  |
| `allowance_type_id` | string |  |
| `approval` | boolean |  |
| `colour` | string |  |
| `company_id` | string |  |
| `created_at` | string |  |
| `description` | string |  |
| `display_icon` | string |  |
| `id` | string |  |
| `name` | string |  |
| `only_admin` | boolean |  |
| `updated_at` | string |  |

## Native endpoint

Through the native Leave Dates API, this operation is `POST /leave-types` (base URL `https://api.leavedates.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-leave-type.md) for the provider-specific parameters and requirements.

