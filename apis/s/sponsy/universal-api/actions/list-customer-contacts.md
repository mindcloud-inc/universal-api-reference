# Sponsy: List Customer Contacts

Retrieves customer contacts from Sponsy.

```
GET https://connect.mindcloud.co/v1/universal/sponsy/latest/actions/list-customer-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sponsy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sponsy/latest/actions/list-customer-contacts?connectionId=$CONNECTION_ID&customerId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customerId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sponsy/latest/actions/list-customer-contacts?${params}`, {
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
| `customerId` | string | yes | Customer ID from Sponsy. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contactable": true,
      "email": "ava@example.com",
      "firstName": "Ava",
      "lastName": "Chen",
      "primary": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contactable` | boolean |  |
| `email` | string |  |
| `firstName` | string |  |
| `lastName` | string |  |
| `primary` | boolean |  |

## Native endpoint

Through the native Sponsy API, this operation is `GET /v1/customers/:customerId/contacts` (base URL `https://api.getsponsy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-customer-contacts.md) for the provider-specific parameters and requirements.

