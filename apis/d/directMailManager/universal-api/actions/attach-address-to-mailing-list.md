# Direct Mail Manager: Attach Address To Mailing List



```
PUT https://connect.mindcloud.co/v1/universal/directMailManager/latest/actions/attach-address-to-mailing-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Direct Mail Manager `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/directMailManager/latest/actions/attach-address-to-mailing-list" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/directMailManager/latest/actions/attach-address-to-mailing-list', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "address_city": "string",
      "address_country": "string",
      "address_line1": "string",
      "address_line2": "string",
      "address_state": "string",
      "address_zip": "string",
      "company": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "first_name": "Ava",
      "id": "string",
      "is_deliverable": true,
      "last_name": "Chen",
      "object": "string",
      "suppressed_at": "2026-05-07T12:00:00.000Z",
      "updated_at": "2026-05-07T12:00:00.000Z",
      "verification_status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address_city` | string |  |
| `address_country` | string |  |
| `address_line1` | string |  |
| `address_line2` | string |  |
| `address_state` | string |  |
| `address_zip` | string |  |
| `company` | string |  |
| `created_at` | date |  |
| `first_name` | string |  |
| `id` | string |  |
| `is_deliverable` | boolean |  |
| `last_name` | string |  |
| `object` | string |  |
| `suppressed_at` | date |  |
| `updated_at` | date |  |
| `verification_status` | string |  |

## Native endpoint

Through the native Direct Mail Manager API, this operation is `POST /addresses/:adr_id/attach` (base URL `https://api.directmailmanager.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/attach-address-to-mailing-list.md) for the provider-specific parameters and requirements.

