# Leave Dates: List Leave Types

Retrieves leave types for a company in Leave Dates.

```
GET https://connect.mindcloud.co/v1/universal/leaveDates/latest/actions/list-leave-types
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Leave Dates `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/leaveDates/latest/actions/list-leave-types?connectionId=$CONNECTION_ID&company=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "company": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/leaveDates/latest/actions/list-leave-types?${params}`, {
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
      "description": "string",
      "display_code": "string",
      "display_icon": "string",
      "id": "string",
      "is_holiday": true,
      "name": "Ava Chen",
      "only_admin": true
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
| `description` | string |  |
| `display_code` | string |  |
| `display_icon` | string |  |
| `id` | string |  |
| `is_holiday` | boolean |  |
| `name` | string |  |
| `only_admin` | boolean |  |

## Native endpoint

Through the native Leave Dates API, this operation is `GET /leave-types` (base URL `https://api.leavedates.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-leave-types.md) for the provider-specific parameters and requirements.

