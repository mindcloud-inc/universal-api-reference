# Peach: Create Contact

Creates a new contact in Peach.

```
POST https://connect.mindcloud.co/v1/universal/peach/latest/actions/create-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Peach `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/peach/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "firstName": "Ava",
  "lastName": "Chen",
  "email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/peach/latest/actions/create-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "firstName": "Ava",
    "lastName": "Chen",
    "email": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `firstName` | string | yes | Contact's first name. |
| `lastName` | string | yes | Contact's last name. |
| `email` | string | yes | Contact's email address. |
| `phone` | string | no | Contact's phone number. |
| `address` | string | no | Contact address. |
| `city` | string | no | Contact city. |
| `street` | string | no | Contact street. |
| `streetNumber` | string | no | Contact street number. |
| `aptNumber` | string | no | Contact apartment number. |
| `zipCode` | string | no | Contact zip code. |
| `groups[]` | array<string> | no | Group names to add to the contact. |
| `customProperties` | object | no | Custom properties for the contact. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contactBody": {
        "accountId": "string",
        "address": "string",
        "aptNumber": "string",
        "city": "string",
        "email": "ava@example.com",
        "firstName": "Ava",
        "lastName": "Chen",
        "source": "string",
        "status": "string",
        "street": "string",
        "streetNumber": "string",
        "telephone": "string",
        "zipCode": "string"
      },
      "contactId": "string",
      "contactResponse": "string",
      "failedCustomProperties": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contactBody` | object | Normalized contact payload Peach persisted. |
| `contactBody.accountId` | string |  |
| `contactBody.address` | string |  |
| `contactBody.aptNumber` | string |  |
| `contactBody.city` | string |  |
| `contactBody.email` | string |  |
| `contactBody.firstName` | string |  |
| `contactBody.lastName` | string |  |
| `contactBody.source` | string |  |
| `contactBody.status` | string |  |
| `contactBody.street` | string |  |
| `contactBody.streetNumber` | string |  |
| `contactBody.telephone` | string |  |
| `contactBody.zipCode` | string |  |
| `contactId` | string |  |
| `contactResponse` | string |  |
| `failedCustomProperties` | object |  |

## Native endpoint

Through the native Peach API, this operation is `POST /contacts` (base URL `https://api.peach-in.com/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contact.md) for the provider-specific parameters and requirements.

