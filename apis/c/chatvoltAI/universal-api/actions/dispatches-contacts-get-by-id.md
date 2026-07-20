# Chatvolt AI: Get Contact by ID

Retrieves a contact from Chatvolt AI.

```
GET https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/dispatches-contacts-get-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chatvolt AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/dispatches-contacts-get-by-id?connectionId=$CONNECTION_ID&contactId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contactId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/dispatches-contacts-get-by-id?${params}`, {
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
| `contactId` | string | yes | The ID of the contact to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contactListId": "string",
      "createdAt": "string",
      "id": "string",
      "name": "Ava Chen",
      "phoneNumber": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contactListId` | string | ContactListId. |
| `createdAt` | string | CreatedAt. |
| `id` | string | Id. |
| `name` | string | Name. |
| `phoneNumber` | string | PhoneNumber. |
| `updatedAt` | string | UpdatedAt. |

## Native endpoint

Through the native Chatvolt AI API, this operation is `GET /dispatches/contacts/{contactId}` (base URL `https://api.chatvolt.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/dispatches-contacts-get-by-id.md) for the provider-specific parameters and requirements.

