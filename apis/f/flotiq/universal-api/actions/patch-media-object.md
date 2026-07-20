# Flotiq: Patch Media Object

Updates part of a media object in Flotiq.

```
PUT https://connect.mindcloud.co/v1/universal/flotiq/latest/actions/patch-media-object
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Flotiq `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/flotiq/latest/actions/patch-media-object" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "body": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/flotiq/latest/actions/patch-media-object', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "body": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The Flotiq media object ID. |
| `body` | object | yes | The partial media object payload. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "alt": "string",
      "extension": "string",
      "externalId": "string",
      "fileName": "Ava Chen",
      "height": 1,
      "id": "string",
      "internal": {},
      "mimeType": "string",
      "size": 1,
      "source": "string",
      "tags": [
        {}
      ],
      "title": "string",
      "type": "string",
      "url": "https://example.com",
      "variants": [
        {}
      ],
      "width": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `alt` | string |  |
| `extension` | string |  |
| `externalId` | string |  |
| `fileName` | string |  |
| `height` | number |  |
| `id` | string |  |
| `internal` | object |  |
| `mimeType` | string |  |
| `size` | number |  |
| `source` | string |  |
| `tags` | array<object> |  |
| `title` | string |  |
| `type` | string |  |
| `url` | string |  |
| `variants` | array<object> |  |
| `width` | number |  |

## Native endpoint

Through the native Flotiq API, this operation is `PATCH /content/_media/{{id}}` (base URL `https://api.flotiq.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/patch-media-object.md) for the provider-specific parameters and requirements.

