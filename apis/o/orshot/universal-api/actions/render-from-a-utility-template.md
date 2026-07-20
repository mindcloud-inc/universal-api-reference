# Orshot: Render from a Utility Template



```
POST https://connect.mindcloud.co/v1/universal/orshot/latest/actions/render-from-a-utility-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Orshot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/orshot/latest/actions/render-from-a-utility-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "renderType": "string",
  "templateId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/orshot/latest/actions/render-from-a-utility-template', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "renderType": "string",
    "templateId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `modifications.delay` | number | no | Delay in milliseconds before capture. |
| `modifications.fullCapture` | boolean | no | Whether to capture the full page when using website screenshot utilities. |
| `modifications.height` | number | no | Output height for the utility render. |
| `modifications.websiteUrl` | string | no | Public website URL used by utility templates like website-screenshot. |
| `modifications.width` | number | no | Output width for the utility render. |
| `renderType` | string | yes | Utility template render type such as images or pdfs. |
| `response.format` | string | no | Format for the generated output. |
| `response.type` | string | no | Return type for the generated output. |
| `templateId` | string | yes | Utility template identifier. |

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
| `data.type` | string | Response type returned by the utility render endpoint. |

## Native endpoint

Through the native Orshot API, this operation is `POST /generate/:renderType` (base URL `https://api.orshot.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/render-from-a-utility-template.md) for the provider-specific parameters and requirements.

