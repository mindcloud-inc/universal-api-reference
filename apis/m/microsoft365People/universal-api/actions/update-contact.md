# Microsoft 365 People: Update Contact

Updates an existing contact in Microsoft 365 People.

```
PUT https://connect.mindcloud.co/v1/universal/microsoft365People/latest/actions/update-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft 365 People `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/microsoft365People/latest/actions/update-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contactId": "AAMkAG..."
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/microsoft365People/latest/actions/update-contact', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contactId": "AAMkAG..."
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contactId` | string | yes | The ID of the Outlook contact to update. Example: `AAMkAG...`. |
| `displayName` | string | no | Updated display name for the contact. Example: `Updated Jamie Royce`. |
| `givenName` | string | no | Updated given name for the contact. Example: `Jamie`. |
| `surname` | string | no | Updated surname for the contact. Example: `Royce`. |
| `emailAddresses[].name` | string | no | Updated display name for the primary email address. Example: `Jamie Royce`. |
| `emailAddresses[].address` | string | no | Updated primary email address for the contact. Example: `jamie@mindcloud.co`. |
| `companyName` | string | no | Updated company name for the contact. Example: `MindCloud`. |
| `jobTitle` | string | no | Updated job title for the contact. Example: `Founder`. |
| `mobilePhone` | string | no | Updated mobile phone number for the contact. Example: `+1 555 555 5555`. |

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

Through the native Microsoft 365 People API, this operation is `PATCH /v1.0/me/contacts/{{contactId}}` (base URL `https://graph.microsoft.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-contact.md) for the provider-specific parameters and requirements.

