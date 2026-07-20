# Stax: List Customers

Retrieves customers from Stax.

```
GET https://connect.mindcloud.co/v1/universal/stax/latest/actions/list-customers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stax `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stax/latest/actions/list-customers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stax/latest/actions/list-customers?${params}`, {
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
      "address1": "string",
      "address2": "string",
      "addressCity": "string",
      "addressState": "string",
      "addressZip": "string",
      "company": "string",
      "createdAt": "string",
      "email": "ava@example.com",
      "firstname": "Ava",
      "id": "string",
      "lastname": "Chen",
      "phone": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address1` | string | Primary street address. |
| `address2` | string | Secondary street address. |
| `addressCity` | string | City. |
| `addressState` | string | State or region. |
| `addressZip` | string | Postal code. |
| `company` | string | Customer company name. |
| `createdAt` | string | Creation timestamp. |
| `email` | string | Customer email address. |
| `firstname` | string | Customer first name. |
| `id` | string | Stax customer identifier. |
| `lastname` | string | Customer last name. |
| `phone` | string | Customer phone number. |
| `updatedAt` | string | Last update timestamp. |

## Native endpoint

Through the native Stax API, this operation is `GET /customer` (base URL `https://apiprod.fattlabs.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-customers.md) for the provider-specific parameters and requirements.

