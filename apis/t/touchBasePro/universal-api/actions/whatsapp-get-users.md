# TouchBasePro: WhatsApp Get Users

Retrieves WhatsApp user records from TouchBasePro.

```
GET https://connect.mindcloud.co/v1/universal/touchBasePro/latest/actions/whatsapp-get-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TouchBasePro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/touchBasePro/latest/actions/whatsapp-get-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/touchBasePro/latest/actions/whatsapp-get-users?${params}`, {
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
      "data": {
        "customers": [
          [
            {}
          ]
        ],
        "hasNextPage": true,
        "limit": 1,
        "offset": 1,
        "totalCustomers": 1
      },
      "message": "string",
      "result": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.customers[]` | array<object> |  |
| `data.customers[].countryCode` | string |  |
| `data.customers[].createdAtUtc` | date |  |
| `data.customers[].customerCreatedAtSource` | string |  |
| `data.customers[].id` | string |  |
| `data.customers[].modifiedAtUtc` | date |  |
| `data.customers[].phoneNumber` | string |  |
| `data.customers[].traits.address.address1` | string |  |
| `data.customers[].traits.address.address2` | string |  |
| `data.customers[].traits.address.city` | string |  |
| `data.customers[].traits.address.country` | string |  |
| `data.customers[].traits.address.state` | string |  |
| `data.customers[].traits.address.zipCode` | string |  |
| `data.customers[].traits.createdAt` | date |  |
| `data.customers[].traits.currency` | string |  |
| `data.customers[].traits.firstName` | string |  |
| `data.customers[].traits.lastName` | string |  |
| `data.customers[].traits.lastOrderId` | number |  |
| `data.customers[].traits.lastOrderName` | string |  |
| `data.customers[].traits.name` | string |  |
| `data.customers[].traits.totalOrdersCount` | number |  |
| `data.customers[].traits.totalSpent` | string |  |
| `data.customers[].traits.whatsappOptedIn` | boolean |  |
| `data.customers[].userId` | string |  |
| `data.hasNextPage` | boolean |  |
| `data.limit` | number |  |
| `data.offset` | number |  |
| `data.totalCustomers` | number |  |
| `message` | string |  |
| `result` | boolean |  |

## Native endpoint

Through the native TouchBasePro API, this operation is `POST /whatsapp/v1/public/apis/users/` (base URL `https://api.touchbasepro.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/whatsapp-get-users.md) for the provider-specific parameters and requirements.

