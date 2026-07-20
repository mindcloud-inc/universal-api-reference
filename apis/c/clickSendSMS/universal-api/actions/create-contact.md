# ClickSend SMS: Create Contact

Creates a new contact in a ClickSend SMS list.

```
POST https://connect.mindcloud.co/v1/universal/clickSendSMS/latest/actions/create-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ClickSend SMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/clickSendSMS/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "list_id": 1,
  "phoneNumber": "string",
  "custom1": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clickSendSMS/latest/actions/create-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "list_id": 1,
    "phoneNumber": "string",
    "custom1": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `list_id` | number | yes | List identifier. |
| `phoneNumber` | string | yes | Contact phone number. |
| `email` | string | no | Contact email. |
| `faxNumber` | string | no | Contact fax number. |
| `firstName` | string | no | Contact first name. |
| `lastName` | string | no | Contact last name. |
| `addressLine1` | string | no | Address line 1. |
| `addressLine2` | string | no | Address line 2. |
| `addressCity` | string | no | Address city. |
| `addressState` | string | no | Address state. |
| `addressPostalCode` | string | no | Address postal code. |
| `addressCountry` | string | no | Address country code. |
| `organizationName` | string | no | Organization name. |
| `custom1` | string | yes | Custom field 1. |
| `custom2` | string | no | Custom field 2. |
| `custom3` | string | no | Custom field 3. |
| `custom4` | string | no | Custom field 4. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `page` | number | no | Page number. |
| `limit` | number | no | Items per page. |

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
      "addressPostalCode": "string",
      "addressState": "string",
      "contactId": 1,
      "custom1": "string",
      "custom2": "string",
      "custom3": "string",
      "custom4": "string",
      "dateAdded": 1,
      "dateUpdated": 1,
      "email": "ava@example.com",
      "faxNumber": "string",
      "firstName": "Ava",
      "lastName": "Chen",
      "listId": 1,
      "listName": "Ava Chen",
      "organizationName": "Ava Chen",
      "phoneNumber": "string"
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
| `addressPostalCode` | string |  |
| `addressState` | string |  |
| `contactId` | number |  |
| `custom1` | string |  |
| `custom2` | string |  |
| `custom3` | string |  |
| `custom4` | string |  |
| `dateAdded` | number |  |
| `dateUpdated` | number |  |
| `email` | string |  |
| `faxNumber` | string |  |
| `firstName` | string |  |
| `lastName` | string |  |
| `listId` | number |  |
| `listName` | string |  |
| `organizationName` | string |  |
| `phoneNumber` | string |  |

## Native endpoint

Through the native ClickSend SMS API, this operation is `POST /v3/lists/:list_id/contacts` (base URL `https://rest.clicksend.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contact.md) for the provider-specific parameters and requirements.

