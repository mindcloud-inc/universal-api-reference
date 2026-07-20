# Notifyre SMS: Create Contact

Creates a new contact in Notifyre.

```
POST https://connect.mindcloud.co/v1/universal/notifyreSMS/latest/actions/create-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Notifyre SMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/notifyreSMS/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "mobileNumber": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/notifyreSMS/latest/actions/create-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "mobileNumber": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `firstName` | string | no | Contact first name. |
| `lastName` | string | no | Contact last name. |
| `mobileNumber` | string | yes | Contact mobile number. |

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
| `id` | string | Created contact identifier. |
| `lastName` | string | Contact last name. |
| `mobileNumber` | string | Contact mobile number. |

## Native endpoint

Through the native Notifyre SMS API, this operation is `POST /addressbook/contacts` (base URL `https://api.notifyre.com/20220711`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contact.md) for the provider-specific parameters and requirements.

