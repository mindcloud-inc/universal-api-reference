# SparrowDesk: Update Contact

Updates an existing contact in SparrowDesk.

```
PUT https://connect.mindcloud.co/v1/universal/sparrowDesk/latest/actions/update-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SparrowDesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/sparrowDesk/latest/actions/update-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sparrowDesk/latest/actions/update-contact', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `companyId` | string | no | Updated SparrowDesk company identifier. |
| `email` | string | no | Updated contact email. |
| `firstName` | string | no | Updated contact first name. |
| `id` | number | yes | SparrowDesk contact ID. |
| `lastName` | string | no | Updated contact last name. |
| `phone` | string | no | Updated contact phone number. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "avatar": "string",
      "blocked": true,
      "city": "string",
      "companyId": 1,
      "companyName": "Ava Chen",
      "country": "string",
      "createdAt": 1,
      "customFields": {},
      "email": "ava@example.com",
      "firstName": "Ava",
      "fullName": "Ava Chen",
      "id": 1,
      "language": "string",
      "lastName": "Chen",
      "phone": "string",
      "properties": {},
      "region": "string",
      "timeZone": "string",
      "unsubscribed": true,
      "updatedAt": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean | Whether the contact is active. |
| `avatar` | string | Avatar URL. |
| `blocked` | boolean | Whether the contact is blocked. |
| `city` | string | City. |
| `companyId` | number | Company ID. |
| `companyName` | string | Company name. |
| `country` | string | Country. |
| `createdAt` | number | Creation timestamp. |
| `customFields` | object | Custom field values. |
| `email` | string | Email address. |
| `firstName` | string | First name. |
| `fullName` | string | Full name. |
| `id` | number | Contact ID. |
| `language` | string | Preferred language. |
| `lastName` | string | Last name. |
| `phone` | string | Phone number. |
| `properties` | object | Contact properties. |
| `region` | string | Region. |
| `timeZone` | string | Preferred time zone. |
| `unsubscribed` | boolean | Whether the contact is unsubscribed. |
| `updatedAt` | number | Last update timestamp. |

## Native endpoint

Through the native SparrowDesk API, this operation is `PATCH /contacts/{{id}}` (base URL `https://api.sparrowdesk.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-contact.md) for the provider-specific parameters and requirements.

