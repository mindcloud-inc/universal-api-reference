# Dwolla: Get Customer

Retrieves details for a customer from Dwolla.

```
GET https://connect.mindcloud.co/v1/universal/dwolla/latest/actions/get-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dwolla `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dwolla/latest/actions/get-customer?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dwolla/latest/actions/get-customer?${params}`, {
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
| `id` | string | no | Dwolla customer ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_links": {},
      "created": "string",
      "email": "ava@example.com",
      "firstName": "Ava",
      "id": "string",
      "lastName": "Chen",
      "status": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_links` | object | HAL links for related customer resources. |
| `created` | string | Customer creation timestamp. |
| `email` | string | Customer email address. |
| `firstName` | string | Customer first name. |
| `id` | string | Dwolla customer identifier. |
| `lastName` | string | Customer last name. |
| `status` | string | Customer status. |
| `type` | string | Dwolla customer type. |

## Native endpoint

Through the native Dwolla API, this operation is `GET /customers/[:id]` (base URL `https://api-sandbox.dwolla.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-customer.md) for the provider-specific parameters and requirements.

