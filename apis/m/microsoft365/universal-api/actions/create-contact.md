# Microsoft 365: Create Contact

Creates a new contact in Microsoft 365.

```
POST https://connect.mindcloud.co/v1/universal/microsoft365/latest/actions/create-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft 365 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/microsoft365/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "displayName": "Jamie Royce"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/microsoft365/latest/actions/create-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "displayName": "Jamie Royce"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `displayName` | string | yes | Display name for the new contact. Example: `Jamie Royce`. |
| `givenName` | string | no | Given name for the new contact. Example: `Jamie`. |
| `surname` | string | no | Surname for the new contact. Example: `Royce`. |
| `emailAddresses[].name` | string | no | Display name for the primary email address. Example: `Jamie Royce`. |
| `emailAddresses[].address` | string | no | Primary email address for the contact. Example: `jamie@mindcloud.co`. |
| `companyName` | string | no | Company name for the contact. Example: `MindCloud`. |
| `jobTitle` | string | no | Job title for the contact. Example: `Founder`. |
| `mobilePhone` | string | no | Mobile phone number for the contact. Example: `+1 555 555 5555`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "companyName": "Ava Chen",
      "displayName": "Ava Chen",
      "emailAddresses": [
        {
          "address": "ava@example.com",
          "name": "ava@example.com"
        }
      ],
      "givenName": "Ava Chen",
      "id": "string",
      "jobTitle": "string",
      "mobilePhone": "string",
      "surname": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `companyName` | string |  |
| `displayName` | string |  |
| `emailAddresses[].address` | string |  |
| `emailAddresses[].name` | string |  |
| `givenName` | string |  |
| `id` | string |  |
| `jobTitle` | string |  |
| `mobilePhone` | string |  |
| `surname` | string |  |

## Native endpoint

Through the native Microsoft 365 API, this operation is `POST /v1.0/me/contacts` (base URL `https://graph.microsoft.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contact.md) for the provider-specific parameters and requirements.

