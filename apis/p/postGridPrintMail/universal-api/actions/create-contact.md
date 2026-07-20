# PostGrid Print & Mail: Create Contact

Creates a contact in PostGrid Print & Mail.

```
POST https://connect.mindcloud.co/v1/universal/postGridPrintMail/latest/actions/create-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PostGrid Print & Mail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/postGridPrintMail/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "addressLine1": "string",
  "countryCode": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/postGridPrintMail/latest/actions/create-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "addressLine1": "string",
    "countryCode": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `firstName` | string | no | The first name for the contact recipient. |
| `companyName` | string | no | The company name for the contact recipient. |
| `lastName` | string | no | The last name for the contact recipient. |
| `addressLine1` | string | yes | The first line of the contact address. |
| `addressLine2` | string | no | The second line of the contact address, if applicable. |
| `city` | string | no | The city for the contact address. |
| `provinceOrState` | string | no | The province or state for the contact address. |
| `postalOrZip` | string | no | The postal or ZIP code for the contact address. |
| `countryCode` | string | yes | The ISO 3166-1 country code for the contact address. |
| `email` | string | no | The email address for the contact. |
| `phoneNumber` | string | no | The phone number for the contact. |
| `jobTitle` | string | no | The job title for the contact. |
| `skipVerification` | boolean | no | Skip PostGrid address verification for this contact. |
| `forceVerifiedStatus` | boolean | no | Force the contact address status to verified. |
| `description` | string | no | An optional description visible in the API and dashboard. |
| `metadata` | object | no | Custom metadata for this contact. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addressLine1": "string",
      "addressStatus": "string",
      "city": "string",
      "country": "string",
      "countryCode": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "firstName": "Ava",
      "id": "string",
      "lastName": "Chen",
      "live": true,
      "mailingLists": [
        {}
      ],
      "object": "string",
      "postalOrZip": "string",
      "provinceOrState": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addressLine1` | string |  |
| `addressStatus` | string |  |
| `city` | string |  |
| `country` | string |  |
| `countryCode` | string |  |
| `createdAt` | date |  |
| `description` | string |  |
| `firstName` | string |  |
| `id` | string |  |
| `lastName` | string |  |
| `live` | boolean |  |
| `mailingLists` | array<object> |  |
| `object` | string |  |
| `postalOrZip` | string |  |
| `provinceOrState` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native PostGrid Print & Mail API, this operation is `POST /contacts` (base URL `https://api.postgrid.com/print-mail/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contact.md) for the provider-specific parameters and requirements.

