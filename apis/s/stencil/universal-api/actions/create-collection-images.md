# Stencil: Create Collection Images



```
POST https://connect.mindcloud.co/v1/universal/stencil/latest/actions/create-collection-images
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stencil `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/stencil/latest/actions/create-collection-images" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/stencil/latest/actions/create-collection-images', {
  method: 'POST',
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
| `collection` | string | no | Collection ID. |
| `metadata` | object | no | Additional metadata returned with the result. |
| `modifications[]` | array<object> | no | Array of modifications applied to the collection output. |
| `select` | number | no | Number of templates to select randomly from the collection. |
| `webhookUrl` | string | no | Webhook URL called when collection images are ready. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "images": [
        {}
      ],
      "metadata": {},
      "modifications": [
        {}
      ],
      "self": "string",
      "status": "string",
      "templates": [
        {}
      ],
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "webhookUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `id` | string |  |
| `images` | array<object> |  |
| `metadata` | object |  |
| `modifications` | array<object> |  |
| `self` | string |  |
| `status` | string |  |
| `templates` | array<object> |  |
| `updatedAt` | date |  |
| `webhookUrl` | string |  |

## Native endpoint

Through the native Stencil API, this operation is `POST /v1/collections` (base URL `https://api.usestencil.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-collection-images.md) for the provider-specific parameters and requirements.

