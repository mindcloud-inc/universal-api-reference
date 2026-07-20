# Chatvolt AI: Create or Update Contact

Creates a contact in Chatvolt AI, or updates an existing one.

```
PUT https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/contacts-create
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chatvolt AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/contacts-create" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/contacts-create', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | no | Include the ID to update an existing contact. Omit to create a new one. |
| `email` | string | no | Email for application/json requests. |
| `phoneNumber` | string | no | PhoneNumber for application/json requests. |
| `firstName` | string | no | FirstName for application/json requests. |
| `lastName` | string | no | LastName for application/json requests. |
| `externalId` | string | no | ExternalId for application/json requests. |
| `picture` | string | no | Picture for application/json requests. |
| `metadata` | object | no | Metadata for application/json requests. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "email": "ava@example.com",
      "externalId": "string",
      "firstName": "Ava",
      "id": "string",
      "lastName": "Chen",
      "metadata": {},
      "organizationId": "string",
      "phoneNumber": "string",
      "picture": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string | CreatedAt. |
| `email` | string | Email. |
| `externalId` | string | ExternalId. |
| `firstName` | string | FirstName. |
| `id` | string | Id. |
| `lastName` | string | LastName. |
| `metadata` | object | Metadata. |
| `organizationId` | string | OrganizationId. |
| `phoneNumber` | string | PhoneNumber. |
| `picture` | string | Picture. |
| `updatedAt` | string | UpdatedAt. |

## Native endpoint

Through the native Chatvolt AI API, this operation is `POST /contacts` (base URL `https://api.chatvolt.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/contacts-create.md) for the provider-specific parameters and requirements.

