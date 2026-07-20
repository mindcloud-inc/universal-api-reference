# Leave Dates: List Companies

Retrieves companies available to the authenticated user in Leave Dates.

```
GET https://connect.mindcloud.co/v1/universal/leaveDates/latest/actions/list-companies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Leave Dates `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/leaveDates/latest/actions/list-companies?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/leaveDates/latest/actions/list-companies?${params}`, {
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
      "allowance_unit_is_days": true,
      "billing_status": "string",
      "current_billing_plan": "string",
      "employments_count": 1,
      "id": "string",
      "minutes_per_working_day": 1,
      "name": "Ava Chen",
      "owner_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allowance_unit_is_days` | boolean |  |
| `billing_status` | string |  |
| `current_billing_plan` | string |  |
| `employments_count` | number |  |
| `id` | string |  |
| `minutes_per_working_day` | number |  |
| `name` | string |  |
| `owner_id` | string |  |

## Native endpoint

Through the native Leave Dates API, this operation is `GET /companies` (base URL `https://api.leavedates.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-companies.md) for the provider-specific parameters and requirements.

