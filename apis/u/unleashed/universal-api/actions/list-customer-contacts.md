# Unleashed: List Customer Contacts

Retrieves customer contacts from Unleashed by customer.

```
GET https://connect.mindcloud.co/v1/universal/unleashed/latest/actions/list-customer-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Unleashed `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/unleashed/latest/actions/list-customer-contacts?connectionId=$CONNECTION_ID&customerGuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customerGuid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/unleashed/latest/actions/list-customer-contacts?${params}`, {
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
| `customerGuid` | string | yes | The Unleashed customer GUID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ddiNumber": "string",
      "deliveryAddress": "string",
      "emailAddress": "ava@example.com",
      "faxNumber": "string",
      "firstName": "Ava",
      "forInvoicing": true,
      "forOrdering": true,
      "forShipping": true,
      "guid": "string",
      "isDefault": true,
      "lastName": "Chen",
      "mobilePhone": "string",
      "notes": "string",
      "officePhone": "string",
      "phoneNumber": "string",
      "tollFreeNumber": "string",
      "website": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ddiNumber` | string |  |
| `deliveryAddress` | string |  |
| `emailAddress` | string |  |
| `faxNumber` | string |  |
| `firstName` | string |  |
| `forInvoicing` | boolean |  |
| `forOrdering` | boolean |  |
| `forShipping` | boolean |  |
| `guid` | string |  |
| `isDefault` | boolean |  |
| `lastName` | string |  |
| `mobilePhone` | string |  |
| `notes` | string |  |
| `officePhone` | string |  |
| `phoneNumber` | string |  |
| `tollFreeNumber` | string |  |
| `website` | string |  |

## Native endpoint

Through the native Unleashed API, this operation is `GET /Customers/:customerGuid/Contacts` (base URL `https://api.unleashedsoftware.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-customer-contacts.md) for the provider-specific parameters and requirements.

