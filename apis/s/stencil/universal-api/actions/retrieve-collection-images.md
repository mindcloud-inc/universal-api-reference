# Stencil: Retrieve Collection Images



```
GET https://connect.mindcloud.co/v1/universal/stencil/latest/actions/retrieve-collection-images
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stencil `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stencil/latest/actions/retrieve-collection-images?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stencil/latest/actions/retrieve-collection-images?${params}`, {
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
| `id` | string | yes | Collection request ID. |

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

Through the native Stencil API, this operation is `GET /v1/collections/:id` (base URL `https://api.usestencil.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-collection-images.md) for the provider-specific parameters and requirements.

