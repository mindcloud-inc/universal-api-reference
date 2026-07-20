# Trust: List Contacts

Retrieves contacts from a Trust workspace.

```
GET https://connect.mindcloud.co/v1/universal/trust/latest/actions/list-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Trust `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/trust/latest/actions/list-contacts?connectionId=$CONNECTION_ID&workspaceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspaceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/trust/latest/actions/list-contacts?${params}`, {
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
| `workspaceId` | string | yes | The Trust workspace id (typeId). |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contactId": "string",
      "created": "string",
      "customerId": "string",
      "email": "ava@example.com",
      "firstName": "Ava",
      "imageUrl": "https://example.com",
      "lastName": "Chen",
      "phone": "string",
      "typeId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contactId` | string |  |
| `created` | string |  |
| `customerId` | string |  |
| `email` | string |  |
| `firstName` | string |  |
| `imageUrl` | string |  |
| `lastName` | string |  |
| `phone` | string |  |
| `typeId` | string |  |

## Native endpoint

Through the native Trust API, this operation is `GET /contacts/all/:workspaceId` (base URL `https://api.usetrust.app/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contacts.md) for the provider-specific parameters and requirements.

