# Productlane: Create Contact

Creates a new contact in Productlane.

```
POST https://connect.mindcloud.co/v1/universal/productlane/latest/actions/create-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Productlane `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/productlane/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/productlane/latest/actions/create-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | yes |  |
| `name` | string | no |  |
| `companyId` | string | no |  |
| `companyName` | string | no |  |
| `companyExternalId` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "companyId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "hubspotId": "string",
      "id": "string",
      "imageUrl": "https://example.com",
      "intercomId": "string",
      "isDeleted": true,
      "name": "Ava Chen",
      "productboardId": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "version": 1,
      "workspaceId": "string",
      "zendeskId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `companyId` | string |  |
| `createdAt` | date |  |
| `email` | string |  |
| `hubspotId` | string |  |
| `id` | string |  |
| `imageUrl` | string |  |
| `intercomId` | string |  |
| `isDeleted` | boolean |  |
| `name` | string |  |
| `productboardId` | string |  |
| `updatedAt` | date |  |
| `version` | number |  |
| `workspaceId` | string |  |
| `zendeskId` | string |  |

## Native endpoint

Through the native Productlane API, this operation is `POST /contacts` (base URL `https://productlane.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contact.md) for the provider-specific parameters and requirements.

