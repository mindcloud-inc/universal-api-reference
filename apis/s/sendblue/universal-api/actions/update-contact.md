# Sendblue: Update Contact

Updates an existing contact in Sendblue.

```
PUT https://connect.mindcloud.co/v1/universal/sendblue/latest/actions/update-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sendblue `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/sendblue/latest/actions/update-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "phoneNumber": "+14155550123"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sendblue/latest/actions/update-contact', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "phoneNumber": "+14155550123"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `phoneNumber` | string | yes | Phone number in E.164 format. Example: `+14155550123`. |
| `firstName` | string | no | Contact's first name. Example: `Taylor`. |
| `lastName` | string | no | Contact's last name. Example: `Kim`. |
| `companyName` | string | no | Company name. Example: `MindCloud`. |
| `customVariables` | object | no | Custom key-value pairs. Keys are human-readable labels; updates merge into the existing set. Example: `[object Object]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contact": {
        "companyName": "Ava Chen",
        "createdAt": "string",
        "firstName": "Ava",
        "lastName": "Chen",
        "phone": "string",
        "sendblueNumber": "string"
      },
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contact.companyName` | string |  |
| `contact.createdAt` | string |  |
| `contact.firstName` | string |  |
| `contact.lastName` | string |  |
| `contact.phone` | string |  |
| `contact.sendblueNumber` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Sendblue API, this operation is `PUT /api/v2/contacts/:phone_number` (base URL `https://api.sendblue.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-contact.md) for the provider-specific parameters and requirements.

