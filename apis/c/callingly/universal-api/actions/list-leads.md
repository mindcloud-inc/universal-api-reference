# Callingly: List Leads

Retrieves leads from Callingly.

```
GET https://connect.mindcloud.co/v1/universal/callingly/latest/actions/list-leads
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Callingly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/callingly/latest/actions/list-leads?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/callingly/latest/actions/list-leads?${params}`, {
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
| `end` | string | no | Filter leads created on or before this date in YYYY-MM-DD format. |
| `phoneNumber` | string | no | Filter leads by phone number. |
| `start` | string | no | Filter leads created on or after this date in YYYY-MM-DD format. |

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
| `lead_owner_id` | number |  |
| `lname` | string |  |
| `phone_number` | string |  |
| `scheduled_call_at` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Callingly API, this operation is `GET /v1/leads` (base URL `https://api.callingly.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-leads.md) for the provider-specific parameters and requirements.

