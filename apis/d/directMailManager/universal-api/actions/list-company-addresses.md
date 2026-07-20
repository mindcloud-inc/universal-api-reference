# Direct Mail Manager: List Company Addresses



```
GET https://connect.mindcloud.co/v1/universal/directMailManager/latest/actions/list-company-addresses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Direct Mail Manager `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/directMailManager/latest/actions/list-company-addresses?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/directMailManager/latest/actions/list-company-addresses?${params}`, {
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

Through the native Direct Mail Manager API, this operation is `GET /company-addresses` (base URL `https://api.directmailmanager.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-company-addresses.md) for the provider-specific parameters and requirements.

