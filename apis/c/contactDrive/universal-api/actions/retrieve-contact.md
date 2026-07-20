# ContactDrive: Retrieve Contact



```
GET https://connect.mindcloud.co/v1/universal/contactDrive/latest/actions/retrieve-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ContactDrive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/contactDrive/latest/actions/retrieve-contact?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/contactDrive/latest/actions/retrieve-contact?${params}`, {
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
| `id` | string | yes | The unique ID for the contact you would like to retrieve |

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

Through the native ContactDrive API, this operation is `GET /contacts` (base URL `https://api.contactdrive.app/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-contact.md) for the provider-specific parameters and requirements.

