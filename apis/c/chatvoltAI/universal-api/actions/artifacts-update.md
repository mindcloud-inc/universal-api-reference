# Chatvolt AI: Update Artifact

Updates an artifact in Chatvolt AI.

```
PUT https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/artifacts-update
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chatvolt AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/artifacts-update" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/artifacts-update', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes |  |
| `name` | string | no | Name for application/json requests. |
| `description` | string | no | Description for application/json requests. |
| `price` | number | no | Price for application/json requests. |
| `externalUrl` | string | no | ExternalUrl for application/json requests. |
| `customJson` | object | no | CustomJson for application/json requests. |
| `categoryId` | string | no | CategoryId for application/json requests. |
| `isActive` | boolean | no | IsActive for application/json requests. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "category": {},
      "categoryId": "string",
      "createdAt": "string",
      "customJson": {},
      "description": "string",
      "externalUrl": "https://example.com",
      "id": "string",
      "isActive": true,
      "media": [
        "string"
      ],
      "name": "Ava Chen",
      "price": 1,
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `category` | object | Category. |
| `categoryId` | string | CategoryId. |
| `createdAt` | string | CreatedAt. |
| `customJson` | object | CustomJson. |
| `description` | string | Description. |
| `externalUrl` | string | ExternalUrl. |
| `id` | string | Id. |
| `isActive` | boolean | IsActive. |
| `media` | array | Media. |
| `name` | string | Name. |
| `price` | number | Price. |
| `updatedAt` | string | UpdatedAt. |

## Native endpoint

Through the native Chatvolt AI API, this operation is `PUT /artifacts/{id}` (base URL `https://api.chatvolt.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/artifacts-update.md) for the provider-specific parameters and requirements.

