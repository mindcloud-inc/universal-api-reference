# Worktivity: Create or Update Customer

Creates or updates a customer in Worktivity.

```
PUT https://connect.mindcloud.co/v1/universal/worktivity/latest/actions/create-or-update-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Worktivity `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/worktivity/latest/actions/create-or-update-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/worktivity/latest/actions/create-or-update-customer', {
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
      "address": "string",
      "createDate": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "id": "string",
      "name": "Ava Chen",
      "notes": "string",
      "phone": "string",
      "surname": "Ava Chen",
      "taxNumber": "string",
      "taxOffice": "string",
      "title": "string",
      "updateDate": "2026-05-07T12:00:00.000Z",
      "website": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string |  |
| `createDate` | date |  |
| `email` | string |  |
| `id` | string |  |
| `name` | string |  |
| `notes` | string |  |
| `phone` | string |  |
| `surname` | string |  |
| `taxNumber` | string |  |
| `taxOffice` | string |  |
| `title` | string |  |
| `updateDate` | date |  |
| `website` | string |  |

## Native endpoint

Through the native Worktivity API, this operation is `POST /Project/AddUpdateCustomer` (base URL `https://open-api.useworktivity.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-or-update-customer.md) for the provider-specific parameters and requirements.

