# Direct Mail Manager: Create Company Address



```
POST https://connect.mindcloud.co/v1/universal/directMailManager/latest/actions/create-company-address
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Direct Mail Manager `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/directMailManager/latest/actions/create-company-address" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/directMailManager/latest/actions/create-company-address', {
  method: 'POST',
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
      "addressCity": "string",
      "addressCountry": "string",
      "addressLine1": "string",
      "addressLine2": "string",
      "addressState": "string",
      "addressZip": "string",
      "company": "string",
      "firstName": "Ava",
      "id": "string",
      "isDefault": true,
      "isRouteDestination": true,
      "lastName": "Chen",
      "object": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addressCity` | string |  |
| `addressCountry` | string |  |
| `addressLine1` | string |  |
| `addressLine2` | string |  |
| `addressState` | string |  |
| `addressZip` | string |  |
| `company` | string |  |
| `firstName` | string |  |
| `id` | string |  |
| `isDefault` | boolean |  |
| `isRouteDestination` | boolean |  |
| `lastName` | string |  |
| `object` | string |  |

## Native endpoint

Through the native Direct Mail Manager API, this operation is `POST /company-addresses` (base URL `https://api.directmailmanager.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-company-address.md) for the provider-specific parameters and requirements.

