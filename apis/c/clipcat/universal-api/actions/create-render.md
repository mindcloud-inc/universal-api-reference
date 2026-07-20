# Clipcat: Create Render

Creates a new video render request in Clipcat.

```
POST https://connect.mindcloud.co/v1/universal/clipcat/latest/actions/create-render
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clipcat `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/clipcat/latest/actions/create-render" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "modifications[]": [
    {
      "text": "Validator test",
      "scene": "Scene 1",
      "object": "_sample_object"
    }
  ],
  "template": "sample-template-uid"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clipcat/latest/actions/create-render', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "modifications[]": [{"text":"Validator test","scene":"Scene 1","object":"_sample_object"}],
    "template": "sample-template-uid"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `metadata` | string | no | Optional metadata to store with the render. |
| `modifications[]` | array<object> | yes | A JSON array of render modifications. Each item can include scene, object, text, color, font-family, background-image, background-color, border-color, border-width, or media_url. Default: `[{"text":"Validator test","scene":"Scene 1","object":"_sample_object"}]`. |
| `template` | string | yes | The template UID to render. Default: `sample-template-uid`. |
| `webhookUrl` | string | no | Optional webhook URL that receives the finished render object. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "string",
      "credits": 1,
      "metadata": "string",
      "modifications": [
        {}
      ],
      "progress": 1,
      "self": "string",
      "status": "string",
      "template": "string",
      "uid": "string",
      "url": "https://example.com",
      "webhook_response_code": 1,
      "webhook_url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | string |  |
| `credits` | number |  |
| `metadata` | string |  |
| `modifications` | array<object> |  |
| `progress` | number |  |
| `self` | string |  |
| `status` | string |  |
| `template` | string |  |
| `uid` | string |  |
| `url` | string |  |
| `webhook_response_code` | number |  |
| `webhook_url` | string |  |

## Native endpoint

Through the native Clipcat API, this operation is `POST /v1/renders` (base URL `https://api.clipcat.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-render.md) for the provider-specific parameters and requirements.

