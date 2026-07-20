# Lexware Office: Retrieve Contact

Retrieves a contact from Lexware Office.

```
GET https://connect.mindcloud.co/v1/universal/lexwareOffice/latest/actions/retrieve-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lexware Office `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lexwareOffice/latest/actions/retrieve-contact?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lexwareOffice/latest/actions/retrieve-contact?${params}`, {
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
| `id` | string | yes | The Lexware contact ID. |

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

Through the native Lexware Office API, this operation is `GET /v1/contacts/:id` (base URL `https://api.lexware.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-contact.md) for the provider-specific parameters and requirements.

