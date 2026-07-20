# LeadDyno: Retrieve Affiliate By Code

Retrieves an affiliate from LeadDyno by affiliate code.

```
GET https://connect.mindcloud.co/v1/universal/leadDyno/latest/actions/retrieve-affiliate-by-code
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LeadDyno `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/leadDyno/latest/actions/retrieve-affiliate-by-code?connectionId=$CONNECTION_ID&affiliate_code=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "affiliate_code": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/leadDyno/latest/actions/retrieve-affiliate-by-code?${params}`, {
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
| `affiliate_code` | string | yes | The affiliate coupon or discount code. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "affiliate_code": "string",
      "affiliate_dashboard_url": "https://example.com",
      "affiliate_url": "https://example.com",
      "archived": true,
      "email": "ava@example.com",
      "first_name": "Ava",
      "id": 1,
      "last_name": "Chen",
      "pending_approval": true,
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `affiliate_code` | string |  |
| `affiliate_dashboard_url` | string |  |
| `affiliate_url` | string |  |
| `archived` | boolean |  |
| `email` | string |  |
| `first_name` | string |  |
| `id` | number |  |
| `last_name` | string |  |
| `pending_approval` | boolean |  |
| `status` | string |  |

## Native endpoint

Through the native LeadDyno API, this operation is `GET /affiliates/by_affiliate_code` (base URL `https://api.leaddyno.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-affiliate-by-code.md) for the provider-specific parameters and requirements.

