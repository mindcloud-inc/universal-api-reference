# ContactDrive: Create Or Update Contact



```
PUT https://connect.mindcloud.co/v1/universal/contactDrive/latest/actions/create-or-update-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ContactDrive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/contactDrive/latest/actions/create-or-update-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/contactDrive/latest/actions/create-or-update-contact', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `data` | object | no | Contact payload envelope described by the ContactDrive legacy API article |
| `data.addresses[]` | array<object> | no | Array of contact address objects with type, street, city, state, zip, and country fields |
| `data.customFields` | object | no | Object of custom field slug keys mapped to contact-specific values |
| `data.emails[]` | array<object> | no | Array of contact email objects with type, address, and isPrimary fields |
| `data.firstName` | string | no | Contact first name |
| `data.fullname` | string | no | Contact full or mailing name |
| `data.gender` | string | no | Contact gender value; docs say Male or Female |
| `data.id` | string | no | ContactDrive system ID for updating an existing contact |
| `data.lastName` | string | no | Contact last name |
| `data.middleName` | string | no | Contact middle name |
| `data.nickname` | string | no | Contact nickname |
| `data.organizations[]` | array<object> | no | Array of contact organization objects with name, jobTitle, and isCurrent fields |
| `data.phones[]` | array<object> | no | Array of contact phone objects with type, number, and isPrimary fields |
| `data.prefix` | string | no | Contact name prefix |
| `data.suffix` | string | no | Contact name suffix |
| `data.tags[]` | array<string> | no | Array of tags associated with the contact |
| `data.transactionTotal` | number | no | Sum of contributions, sales, or other transactions for the contact |
| `data.websites[]` | array<object> | no | Array of contact website objects with name and URL fields |

## Response

```json
{
  "success": true,
  "data": [
    {
      "city": "string",
      "company": "string",
      "contactedAt": "2026-05-07T12:00:00.000Z",
      "country": "string",
      "county": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "customFields": {},
      "emailAddress": "ava@example.com",
      "firstName": "Ava",
      "fullname": "Ava Chen",
      "gender": "string",
      "id": "string",
      "jobTitle": "string",
      "lastName": "Chen",
      "middleName": "Ava Chen",
      "nickname": "Ava Chen",
      "phone": "string",
      "prefix": "string",
      "state": "string",
      "street": "string",
      "suffix": "string",
      "tags": [
        [
          "string"
        ]
      ],
      "transactionTotal": 1,
      "zip": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `city` | string | Primary city |
| `company` | string | Contact company or employer |
| `contactedAt` | date | Last contacted timestamp |
| `country` | string | Primary country |
| `county` | string | Primary county |
| `createdAt` | date | Contact created timestamp |
| `customFields` | object | Custom field values |
| `emailAddress` | string | Primary email address |
| `firstName` | string | Contact first name |
| `fullname` | string | Contact full or mailing name |
| `gender` | string | Contact gender |
| `id` | string | ContactDrive contact ID |
| `jobTitle` | string | Contact job title or occupation |
| `lastName` | string | Contact last name |
| `middleName` | string | Contact middle name |
| `nickname` | string | Contact nickname |
| `phone` | string | Primary phone number |
| `prefix` | string | Contact name prefix |
| `state` | string | Primary state or province |
| `street` | string | Primary street address |
| `suffix` | string | Contact name suffix |
| `tags[]` | array<string> | Contact tags |
| `transactionTotal` | number | Total transaction value |
| `zip` | string | Primary ZIP or postal code |

## Native endpoint

Through the native ContactDrive API, this operation is `POST /contacts` (base URL `https://api.contactdrive.app/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-or-update-contact.md) for the provider-specific parameters and requirements.

