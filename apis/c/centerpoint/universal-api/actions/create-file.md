# Centerpoint: Create File



```
POST https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/create-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Centerpoint `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/create-file" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "data": {},
  "data.attributes": {},
  "data.attributes.url": "https://example.com",
  "data.attributes.title": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/create-file', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "data": {},
    "data.attributes": {},
    "data.attributes.url": "https://example.com",
    "data.attributes.title": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `data` | object | yes |  |
| `data.attributes` | object | yes |  |
| `data.attributes.url` | string | yes |  |
| `data.attributes.title` | string | yes |  |
| `data.attributes.description` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "createdAt": "string",
        "deletedAt": {},
        "height": 1,
        "latitude": 1,
        "longitude": 1,
        "mimeType": "string",
        "thumbnailUrl": {},
        "title": {},
        "updatedAt": "string",
        "url": "https://example.com",
        "variety": "string",
        "width": 1
      },
      "id": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes.createdAt` | string |  |
| `attributes.deletedAt` | object |  |
| `attributes.height` | number |  |
| `attributes.latitude` | number |  |
| `attributes.longitude` | number |  |
| `attributes.mimeType` | string |  |
| `attributes.thumbnailUrl` | object |  |
| `attributes.title` | object |  |
| `attributes.updatedAt` | string |  |
| `attributes.url` | string |  |
| `attributes.variety` | string |  |
| `attributes.width` | number |  |
| `id` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Centerpoint API, this operation is `POST files` (base URL `https://api.centerpointconnect.io/centerpoint/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-file.md) for the provider-specific parameters and requirements.

