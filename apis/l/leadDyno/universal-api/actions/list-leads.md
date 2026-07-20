# LeadDyno: List Leads

Retrieves leads from your LeadDyno account.

```
GET https://connect.mindcloud.co/v1/universal/leadDyno/latest/actions/list-leads
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LeadDyno `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/leadDyno/latest/actions/list-leads?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/leadDyno/latest/actions/list-leads?${params}`, {
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
      "affiliate": {},
      "campaign": {},
      "created_at": "string",
      "email": "ava@example.com",
      "first_name": "Ava",
      "id": 1,
      "last_name": "Chen",
      "latest_visitor": {},
      "status": "string",
      "tracking_code": "string",
      "updated_at": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `affiliate` | object |  |
| `campaign` | object |  |
| `created_at` | string |  |
| `email` | string |  |
| `first_name` | string |  |
| `id` | number |  |
| `last_name` | string |  |
| `latest_visitor` | object |  |
| `status` | string |  |
| `tracking_code` | string |  |
| `updated_at` | string |  |

## Native endpoint

Through the native LeadDyno API, this operation is `GET /leads` (base URL `https://api.leaddyno.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-leads.md) for the provider-specific parameters and requirements.

