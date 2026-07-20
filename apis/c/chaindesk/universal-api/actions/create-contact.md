# Chaindesk: Create Contact

Creates a new contact in Chaindesk.

```
POST https://connect.mindcloud.co/v1/universal/chaindesk/latest/actions/create-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chaindesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/chaindesk/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "draftConfig": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chaindesk/latest/actions/create-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "draftConfig": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `draftConfig` | object<object> | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "agentId": "string",
      "createdAt": "string",
      "email": "ava@example.com",
      "externalId": "string",
      "firstName": "Ava",
      "id": "string",
      "lastName": "Chen",
      "metadata": "string",
      "organizationId": "string",
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
| `agentId` | string |  |
| `createdAt` | string |  |
| `email` | string |  |
| `externalId` | string |  |
| `firstName` | string |  |
| `id` | string |  |
| `lastName` | string |  |
| `metadata` | string |  |
| `organizationId` | string |  |
| `phoneNumber` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Chaindesk API, this operation is `POST /contacts` (base URL `https://app.chaindesk.ai/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contact.md) for the provider-specific parameters and requirements.

