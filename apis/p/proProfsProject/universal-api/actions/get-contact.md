# ProProfs Project: Get Contact

Retrieves a contact from ProProfs Project.

```
GET https://connect.mindcloud.co/v1/universal/proProfsProject/latest/actions/get-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ProProfs Project `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/proProfsProject/latest/actions/get-contact?connectionId=$CONNECTION_ID&contactId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contactId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/proProfsProject/latest/actions/get-contact?${params}`, {
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
| `contactId` | string | yes | The contact ID to fetch. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "clientId": "string",
      "companyName": "Ava Chen",
      "contactId": "string",
      "contactName": "Ava Chen",
      "dateCreated": "string",
      "dateModified": "string",
      "email": "ava@example.com",
      "fax": "string",
      "mobile": "string",
      "role": "string",
      "tel": "string",
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `clientId` | string |  |
| `companyName` | string |  |
| `contactId` | string |  |
| `contactName` | string |  |
| `dateCreated` | string |  |
| `dateModified` | string |  |
| `email` | string |  |
| `fax` | string |  |
| `mobile` | string |  |
| `role` | string |  |
| `tel` | string |  |
| `userId` | string |  |

## Native endpoint

Through the native ProProfs Project API, this operation is `GET /contacts/{{contact_id}}` (base URL `https://api.projectbubble.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact.md) for the provider-specific parameters and requirements.

