# Flotiq: Get Media Object

Retrieves a media object from Flotiq.

```
GET https://connect.mindcloud.co/v1/universal/flotiq/latest/actions/get-media-object
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Flotiq `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/flotiq/latest/actions/get-media-object?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/flotiq/latest/actions/get-media-object?${params}`, {
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
| `id` | string | yes | The Flotiq media object ID. |

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

Through the native Flotiq API, this operation is `GET /content/_media/{{id}}` (base URL `https://api.flotiq.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-media-object.md) for the provider-specific parameters and requirements.

