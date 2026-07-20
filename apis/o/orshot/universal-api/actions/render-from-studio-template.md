# Orshot: Render from Studio Template



```
POST https://connect.mindcloud.co/v1/universal/orshot/latest/actions/render-from-studio-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Orshot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/orshot/latest/actions/render-from-studio-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "templateId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/orshot/latest/actions/render-from-studio-template', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "templateId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `templateId` | number | yes | Studio template identifier to render. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "content": "string",
        "format": "string",
        "responseTime": 1,
        "type": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.content` | string | Rendered output payload in the requested response type. |
| `data.format` | string | Output format for the rendered asset. |
| `data.responseTime` | number | Render time reported by Orshot in milliseconds. |
| `data.type` | string | Response type returned by the render endpoint. |

## Native endpoint

Through the native Orshot API, this operation is `POST /studio/render` (base URL `https://api.orshot.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/render-from-studio-template.md) for the provider-specific parameters and requirements.

