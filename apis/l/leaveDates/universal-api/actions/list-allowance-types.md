# Leave Dates: List Allowance Types

Retrieves allowance types for a company in Leave Dates.

```
GET https://connect.mindcloud.co/v1/universal/leaveDates/latest/actions/list-allowance-types
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Leave Dates `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/leaveDates/latest/actions/list-allowance-types?connectionId=$CONNECTION_ID&company=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "company": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/leaveDates/latest/actions/list-allowance-types?${params}`, {
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
      "breakdown_types": [
        {}
      ],
      "company_id": "string",
      "created_at": "string",
      "description": "string",
      "id": "string",
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
| `breakdown_types` | array<object> |  |
| `company_id` | string |  |
| `created_at` | string |  |
| `description` | string |  |
| `id` | string |  |
| `name` | string |  |
| `updated_at` | string |  |

## Native endpoint

Through the native Leave Dates API, this operation is `GET /allowance-types` (base URL `https://api.leavedates.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-allowance-types.md) for the provider-specific parameters and requirements.

