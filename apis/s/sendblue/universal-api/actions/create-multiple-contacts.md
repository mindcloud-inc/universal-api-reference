# Sendblue: Create Multiple Contacts

Creates multiple contacts in Sendblue.

```
POST https://connect.mindcloud.co/v1/universal/sendblue/latest/actions/create-multiple-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sendblue `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sendblue/latest/actions/create-multiple-contacts" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contacts[]": "[object Object]",
  "contacts[].phone": "+14155550123"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sendblue/latest/actions/create-multiple-contacts', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contacts[]": "[object Object]",
    "contacts[].phone": "+14155550123"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contacts[]` | array<object> | yes | Array of contact objects to create in bulk. Example: `[object Object]`. |
| `contacts[].phone` | string | yes | Contact phone number in E.164 format. Example: `+14155550123`. |
| `contacts[].firstName` | string | no | Contact's first name. Example: `Taylor`. |
| `contacts[].lastName` | string | no | Contact's last name. Example: `Kim`. |
| `contacts[].companyName` | string | no | Company name. Example: `MindCloud`. |
| `contacts[].customVariables` | object | no | Custom key-value pairs for each contact. Example: `[object Object]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contacts": [
        {
          "companyName": "Ava Chen",
          "createdAt": "string",
          "firstName": "Ava",
          "lastName": "Chen",
          "phone": "string"
        }
      ],
      "numberOfContactsCreated": 1,
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contacts[].companyName` | string |  |
| `contacts[].createdAt` | string |  |
| `contacts[].firstName` | string |  |
| `contacts[].lastName` | string |  |
| `contacts[].phone` | string |  |
| `numberOfContactsCreated` | number |  |
| `status` | string |  |

## Native endpoint

Through the native Sendblue API, this operation is `POST /api/v2/contacts/bulk` (base URL `https://api.sendblue.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-multiple-contacts.md) for the provider-specific parameters and requirements.

