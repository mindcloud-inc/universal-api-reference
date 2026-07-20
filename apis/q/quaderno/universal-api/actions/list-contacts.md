# Quaderno: List Contacts

Retrieves contact records from Quaderno.

```
GET https://connect.mindcloud.co/v1/universal/quaderno/latest/actions/list-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Quaderno `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quaderno/latest/actions/list-contacts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/quaderno/latest/actions/list-contacts?${params}`, {
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
| `processorId` | string | no | Filter contacts by processor ID. |
| `q` | string | no | Filter contacts by full name, email, or tax ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "city": "string",
      "country": "string",
      "createdAt": 1,
      "email": "ava@example.com",
      "firstName": "Ava",
      "fullName": "Ava Chen",
      "id": 1,
      "kind": "string",
      "language": "string",
      "lastName": {},
      "notes": {},
      "permalink": "https://example.com",
      "phone1": {},
      "postalCode": "string",
      "processor": {},
      "processorId": {},
      "region": "string",
      "streetLine1": "string",
      "streetLine2": {},
      "taxId": {},
      "taxStatus": "string",
      "web": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `city` | string |  |
| `country` | string |  |
| `createdAt` | number |  |
| `email` | string |  |
| `firstName` | string |  |
| `fullName` | string |  |
| `id` | number |  |
| `kind` | string |  |
| `language` | string |  |
| `lastName` | object |  |
| `notes` | object |  |
| `permalink` | string |  |
| `phone1` | object |  |
| `postalCode` | string |  |
| `processor` | object |  |
| `processorId` | object |  |
| `region` | string |  |
| `streetLine1` | string |  |
| `streetLine2` | object |  |
| `taxId` | object |  |
| `taxStatus` | string |  |
| `web` | object |  |

## Native endpoint

Through the native Quaderno API, this operation is `GET /contacts` (base URL `https://sandbox-quadernoapp.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contacts.md) for the provider-specific parameters and requirements.

