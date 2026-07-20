# SparrowDesk: Get Contact

Retrieves a contact from SparrowDesk.

```
GET https://connect.mindcloud.co/v1/universal/sparrowDesk/latest/actions/get-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SparrowDesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sparrowDesk/latest/actions/get-contact?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sparrowDesk/latest/actions/get-contact?${params}`, {
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
| `id` | number | yes | SparrowDesk contact ID. |

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

Through the native SparrowDesk API, this operation is `GET /contacts/{{id}}` (base URL `https://api.sparrowdesk.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact.md) for the provider-specific parameters and requirements.

