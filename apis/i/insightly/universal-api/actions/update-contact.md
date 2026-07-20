# Insightly: Update Contact

Updates an existing contact in Insightly.

```
PUT https://connect.mindcloud.co/v1/universal/insightly/latest/actions/update-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Insightly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/insightly/latest/actions/update-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contactId": 1,
  "firstName": "Ava"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/insightly/latest/actions/update-contact', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contactId": 1,
    "firstName": "Ava"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contactId` | number | yes | The Contact ID to update. |
| `firstName` | string | yes | The contact's first name. |
| `lastName` | string | no | The contact's last name. |
| `emailAddress` | string | no | The contact's email address. |
| `phone` | string | no | The contact's primary phone number. |
| `title` | string | no | The contact's job title. |
| `organisationId` | number | no | The related Organisation ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contactId": 1,
      "createdUserId": 1,
      "dateCreatedUtc": "2026-05-07T12:00:00.000Z",
      "dateUpdatedUtc": "2026-05-07T12:00:00.000Z",
      "emailAddress": "ava@example.com",
      "emailOptedOut": true,
      "firstName": "Ava",
      "imageUrl": "https://example.com",
      "lastActivityDateUtc": "2026-05-07T12:00:00.000Z",
      "lastName": "Chen",
      "nextActivityDateUtc": "2026-05-07T12:00:00.000Z",
      "organisationId": 1,
      "ownerUserId": 1,
      "phone": "string",
      "title": "string",
      "visibleTo": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contactId` | number |  |
| `createdUserId` | number |  |
| `dateCreatedUtc` | date |  |
| `dateUpdatedUtc` | date |  |
| `emailAddress` | string |  |
| `emailOptedOut` | boolean |  |
| `firstName` | string |  |
| `imageUrl` | string |  |
| `lastActivityDateUtc` | date |  |
| `lastName` | string |  |
| `nextActivityDateUtc` | date |  |
| `organisationId` | number |  |
| `ownerUserId` | number |  |
| `phone` | string |  |
| `title` | string |  |
| `visibleTo` | string |  |

## Native endpoint

Through the native Insightly API, this operation is `PUT {{credentials.apiBaseUrl}}Contacts` (base URL `https://api.na1.insightly.com/v3.1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-contact.md) for the provider-specific parameters and requirements.

