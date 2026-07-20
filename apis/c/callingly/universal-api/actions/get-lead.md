# Callingly: Get Lead

Retrieves a lead from Callingly.

```
GET https://connect.mindcloud.co/v1/universal/callingly/latest/actions/get-lead
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Callingly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/callingly/latest/actions/get-lead?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/callingly/latest/actions/get-lead?${params}`, {
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
| `id` | number | yes | The Callingly lead ID to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "account_id": 1,
      "category": "string",
      "company": "string",
      "created_at": "string",
      "email": "ava@example.com",
      "fname": "Ava Chen",
      "id": 1,
      "is_blocked": 1,
      "is_stopped": 1,
      "lead_owner_id": 1,
      "lname": "Ava Chen",
      "phone_number": "string",
      "scheduled_call_at": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account_id` | number |  |
| `category` | string |  |
| `company` | string |  |
| `created_at` | string |  |
| `email` | string |  |
| `fname` | string |  |
| `id` | number |  |
| `is_blocked` | number |  |
| `is_stopped` | number |  |
| `lead_owner_id` | number |  |
| `lname` | string |  |
| `phone_number` | string |  |
| `scheduled_call_at` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Callingly API, this operation is `GET /v1/leads/{{id}}` (base URL `https://api.callingly.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-lead.md) for the provider-specific parameters and requirements.

