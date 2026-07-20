# Notifyre SMS: Get Contact

Retrieves a contact from Notifyre address book.

```
GET https://connect.mindcloud.co/v1/universal/notifyreSMS/latest/actions/get-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Notifyre SMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/notifyreSMS/latest/actions/get-contact?connectionId=$CONNECTION_ID&contactId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contactId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/notifyreSMS/latest/actions/get-contact?${params}`, {
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
| `contactId` | string | yes | Contact identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "firstName": "Ava",
      "groups": [
        {}
      ],
      "id": "string",
      "lastName": "Chen",
      "mobileNumber": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `firstName` | string | Contact first name. |
| `groups` | array<object> | Groups assigned to the contact. |
| `id` | string | Contact identifier. |
| `lastName` | string | Contact last name. |
| `mobileNumber` | string | Contact mobile number. |

## Native endpoint

Through the native Notifyre SMS API, this operation is `GET /addressbook/contacts/:contactId` (base URL `https://api.notifyre.com/20220711`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact.md) for the provider-specific parameters and requirements.

