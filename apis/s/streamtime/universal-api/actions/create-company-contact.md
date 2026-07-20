# Streamtime: Create Company Contact



```
POST https://connect.mindcloud.co/v1/universal/streamtime/latest/actions/create-company-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Streamtime `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/streamtime/latest/actions/create-company-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "companyId": "711949",
  "contactStatus.id": "1"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/streamtime/latest/actions/create-company-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "companyId": "711949",
    "contactStatus.id": "1"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `companyId` | number | yes | Company ID Example: `711949`. |
| `firstName` | string | no | First name Example: `Jane`. |
| `lastName` | string | no | Last name Example: `Doe`. |
| `email` | string | no | Email address Example: `jane.doe@example.com`. |
| `phoneNumber` | string | no | Phone number Example: `+64 21 123 4567`. |
| `position` | string | no | Position or job title Example: `Project Manager`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contactStatus` | object | no | Status of a contact |
| `contactStatus.id` | number | yes | Contact status ID Example: `1`. |
| `contactLabels[]` | array<object> | no | Labels applied to the contact |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "companyId": 1,
      "contactStatus": {},
      "email": "ava@example.com",
      "firstName": "Ava",
      "id": 1,
      "lastName": "Chen",
      "notes": "string",
      "phoneNumber": "string",
      "position": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean | Is contact active |
| `companyId` | number | Company ID |
| `contactStatus` | object | Contact status |
| `email` | string | Email address |
| `firstName` | string | First name |
| `id` | number | Contact ID |
| `lastName` | string | Last name |
| `notes` | string | Notes |
| `phoneNumber` | string | Phone number |
| `position` | string | Position |

## Native endpoint

Through the native Streamtime API, this operation is `POST /companies/:company_id/contacts` (base URL `https://api.streamtime.net/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-company-contact.md) for the provider-specific parameters and requirements.

