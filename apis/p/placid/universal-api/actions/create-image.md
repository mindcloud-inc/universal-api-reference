# Placid: Create Image

Creates a new image in Placid from a template.

```
POST https://connect.mindcloud.co/v1/universal/placid/latest/actions/create-image
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Placid `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/placid/latest/actions/create-image" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/placid/latest/actions/create-image', {
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
| `templateUuid` | string | no |  |
| `webhookSuccess` | string | no |  |
| `createNow` | boolean | no |  |
| `passthrough` | string | no |  |
| `layers` | object | no |  |
| `transfer` | object | no |  |
| `modifications` | object | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "errors": [
        {}
      ],
      "id": 1,
      "imageUrl": "https://example.com",
      "passthrough": "string",
      "pollingUrl": "https://example.com",
      "status": "string",
      "transferUrl": "https://example.com",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `errors` | array<object> |  |
| `id` | number |  |
| `imageUrl` | string |  |
| `passthrough` | string |  |
| `pollingUrl` | string |  |
| `status` | string |  |
| `transferUrl` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Placid API, this operation is `POST /api/rest/images` (base URL `https://api.placid.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-image.md) for the provider-specific parameters and requirements.

