# Lexware Office: Create Contact

Creates a new contact in Lexware Office.

```
POST https://connect.mindcloud.co/v1/universal/lexwareOffice/latest/actions/create-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lexware Office `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/lexwareOffice/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "version": "0"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lexwareOffice/latest/actions/create-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "version": "0"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `version` | number | yes | The contact version. Set to 0 when creating a new contact. Default: `0`. |
| `roles.customer` | object | no | Pass an empty object to assign the customer role. Default: `{}`. |
| `roles.vendor` | object | no | Pass an empty object to assign the vendor role. |
| `company.name` | string | no | The company name for company contacts. |
| `person.salutation` | string | no | The person salutation. |
| `person.firstName` | string | no | The person first name. |
| `person.lastName` | string | no | The person last name. |
| `note` | string | no | An internal note for the contact. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdDate": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "resourceUri": "string",
      "updatedDate": "2026-05-07T12:00:00.000Z",
      "version": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdDate` | date |  |
| `id` | string |  |
| `resourceUri` | string |  |
| `updatedDate` | date |  |
| `version` | number |  |

## Native endpoint

Through the native Lexware Office API, this operation is `POST /v1/contacts` (base URL `https://api.lexware.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contact.md) for the provider-specific parameters and requirements.

