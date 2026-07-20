# Formitize: List Contacts

Retrieves contacts from Formitize.

```
GET https://connect.mindcloud.co/v1/universal/formitize/latest/actions/list-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Formitize `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/formitize/latest/actions/list-contacts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/formitize/latest/actions/list-contacts?${params}`, {
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
| `clientId` | string | no | Formitize client ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "custom": [
        {}
      ],
      "email": "ava@example.com",
      "firstName": "Ava",
      "homePhone": "string",
      "homePhoneAreaCode": "string",
      "id": "string",
      "lastName": "Chen",
      "mobile": "string",
      "mobileAreaCode": "string",
      "workPhone": "string",
      "workPhoneAreaCode": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `custom` | array<object> |  |
| `email` | string |  |
| `firstName` | string |  |
| `homePhone` | string |  |
| `homePhoneAreaCode` | string |  |
| `id` | string |  |
| `lastName` | string |  |
| `mobile` | string |  |
| `mobileAreaCode` | string |  |
| `workPhone` | string |  |
| `workPhoneAreaCode` | string |  |

## Native endpoint

Through the native Formitize API, this operation is `GET /crm/client/:clientID/contact/` (base URL `https://service.formitize.com/api/rest/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contacts.md) for the provider-specific parameters and requirements.

