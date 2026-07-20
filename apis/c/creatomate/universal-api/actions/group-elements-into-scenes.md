# Creatomate: Group Elements Into Scenes

Creates a render that groups elements into scenes.

```
POST https://connect.mindcloud.co/v1/universal/creatomate/latest/actions/group-elements-into-scenes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Creatomate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/creatomate/latest/actions/group-elements-into-scenes" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "scenes[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/creatomate/latest/actions/group-elements-into-scenes', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "scenes[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `scenes[]` | array<object> | yes | Ordered list of scene objects. Each scene should include `audioSource` and `imageSource`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `logoOverlayUrl` | string | no | Optional logo image URL to overlay across every scene. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "outputFormat": "string",
      "status": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Creatomate render ID. |
| `outputFormat` | string | Output format requested for the render. |
| `status` | string | Current render status returned by Creatomate. |
| `url` | string | Direct URL for the rendered output file. |

## Native endpoint

Through the native Creatomate API, this operation is `POST /v2/renders` (base URL `https://api.creatomate.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/group-elements-into-scenes.md) for the provider-specific parameters and requirements.

