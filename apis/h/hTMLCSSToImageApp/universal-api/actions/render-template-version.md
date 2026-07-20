# HTML/CSS to Image app: Render Template Version



```
POST https://connect.mindcloud.co/v1/universal/hTMLCSSToImageApp/latest/actions/render-template-version
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HTML/CSS to Image app `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/hTMLCSSToImageApp/latest/actions/render-template-version" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "templateId": "string",
  "templateVersion": 1,
  "templateValues": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hTMLCSSToImageApp/latest/actions/render-template-version', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "templateId": "string",
    "templateVersion": 1,
    "templateValues": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `templateId` | string | yes | Identifier of the template to render. |
| `templateVersion` | number | yes | Specific template version to render. |
| `templateValues` | object | yes | Object of values to substitute into the template. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Rendered image identifier. |
| `url` | string | Permanent URL for the rendered template image. |

## Native endpoint

Through the native HTML/CSS to Image app API, this operation is `POST /v1/image/:templateId/:templateVersion` (base URL `https://hcti.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/render-template-version.md) for the provider-specific parameters and requirements.

