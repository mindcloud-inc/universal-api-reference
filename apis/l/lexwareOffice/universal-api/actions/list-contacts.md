# Lexware Office: List Contacts

Retrieves a list of contacts from Lexware Office.

```
GET https://connect.mindcloud.co/v1/universal/lexwareOffice/latest/actions/list-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lexware Office `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lexwareOffice/latest/actions/list-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lexwareOffice/latest/actions/list-contacts?${params}`, {
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
| `email` | string | no | Filter contacts by matching email address. |
| `name` | string | no | Filter contacts by matching contact name. |
| `number` | number | no | Filter contacts by customer or vendor number. |
| `customer` | boolean | no | Filter by whether the contact has the customer role. |
| `vendor` | boolean | no | Filter by whether the contact has the vendor role. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "id": "string",
      "note": "string",
      "organizationId": "string",
      "person": {
        "firstName": "Ava",
        "lastName": "Chen",
        "salutation": "string"
      },
      "roles": {
        "customer": {
          "number": 1
        }
      },
      "version": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean |  |
| `id` | string |  |
| `note` | string |  |
| `organizationId` | string |  |
| `person` | object |  |
| `person.firstName` | string |  |
| `person.lastName` | string |  |
| `person.salutation` | string |  |
| `roles` | object |  |
| `roles.customer` | object |  |
| `roles.customer.number` | number |  |
| `version` | number |  |

## Native endpoint

Through the native Lexware Office API, this operation is `GET /v1/contacts` (base URL `https://api.lexware.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-contacts.md) for the provider-specific parameters and requirements.

