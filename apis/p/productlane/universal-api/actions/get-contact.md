# Productlane: Get Contact

Retrieves a contact from your Productlane workspace.

```
GET https://connect.mindcloud.co/v1/universal/productlane/latest/actions/get-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Productlane `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/productlane/latest/actions/get-contact?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/productlane/latest/actions/get-contact?${params}`, {
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
| `id` | string | yes |  |

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

Through the native Productlane API, this operation is `GET /contacts/:id` (base URL `https://productlane.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact.md) for the provider-specific parameters and requirements.

