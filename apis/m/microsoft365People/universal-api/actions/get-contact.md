# Microsoft 365 People: Get Contact

Retrieves a contact from Microsoft 365 People.

```
GET https://connect.mindcloud.co/v1/universal/microsoft365People/latest/actions/get-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft 365 People `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/microsoft365People/latest/actions/get-contact?connectionId=$CONNECTION_ID&contactId=AAMkAG..." \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contactId": "AAMkAG..."
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/microsoft365People/latest/actions/get-contact?${params}`, {
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
| `contactId` | string | yes | The ID of the Outlook contact. Example: `AAMkAG...`. |

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

Through the native Microsoft 365 People API, this operation is `GET /v1.0/me/contacts/{{contactId}}` (base URL `https://graph.microsoft.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact.md) for the provider-specific parameters and requirements.

