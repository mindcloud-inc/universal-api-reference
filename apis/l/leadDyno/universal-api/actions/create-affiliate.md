# LeadDyno: Create Affiliate

Creates a new affiliate in LeadDyno.

```
POST https://connect.mindcloud.co/v1/universal/leadDyno/latest/actions/create-affiliate
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LeadDyno `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/leadDyno/latest/actions/create-affiliate" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/leadDyno/latest/actions/create-affiliate', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `affiliate_code` | string | no | A custom affiliate code for the new affiliate. |
| `email` | string | yes | The email address of the new affiliate. |
| `first_name` | string | no | The first name of the affiliate. |
| `last_name` | string | no | The last name of the affiliate. |

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

Through the native LeadDyno API, this operation is `POST /affiliates` (base URL `https://api.leaddyno.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-affiliate.md) for the provider-specific parameters and requirements.

