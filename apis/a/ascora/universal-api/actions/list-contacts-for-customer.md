# Ascora: List Contacts For Customer

Retrieves contacts for a customer from Ascora.

```
GET https://connect.mindcloud.co/v1/universal/ascora/latest/actions/list-contacts-for-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ascora `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ascora/latest/actions/list-contacts-for-customer?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ascora/latest/actions/list-contacts-for-customer?${params}`, {
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
| `customerId` | string | no | Ascora customer ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "results": [
        {}
      ],
      "success": true,
      "totalPages": 1,
      "totalRecords": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `results` | array<object> | Contacts linked to the selected customer. |
| `success` | boolean | Whether Ascora returned the customer contacts successfully. |
| `totalPages` | number | Total result pages returned by Ascora. |
| `totalRecords` | number | Total matching contacts. |

## Native endpoint

Through the native Ascora API, this operation is `GET /Customers/GetContactsForCustomer/{{customerId}}` (base URL `https://api.ascora.com.au`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contacts-for-customer.md) for the provider-specific parameters and requirements.

