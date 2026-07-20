# Templated: List Renders

Retrieves all render records from Templated.

```
GET https://connect.mindcloud.co/v1/universal/templated/latest/actions/list-renders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Templated `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/templated/latest/actions/list-renders?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/templated/latest/actions/list-renders?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "externalId": "string",
      "format": "string",
      "height": 1,
      "id": "string",
      "name": "Ava Chen",
      "page": "string",
      "payload": "string",
      "render_url": "https://example.com",
      "status": "string",
      "templateId": "string",
      "templateName": "Ava Chen",
      "url": "https://example.com",
      "width": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `externalId` | string |  |
| `format` | string |  |
| `height` | number |  |
| `id` | string |  |
| `name` | string |  |
| `page` | string |  |
| `payload` | string |  |
| `render_url` | string |  |
| `status` | string |  |
| `templateId` | string |  |
| `templateName` | string |  |
| `url` | string |  |
| `width` | number |  |

## Native endpoint

Through the native Templated API, this operation is `GET /v1/renders` (base URL `https://api.templated.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-renders.md) for the provider-specific parameters and requirements.

