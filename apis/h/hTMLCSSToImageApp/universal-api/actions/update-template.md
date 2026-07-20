# HTML/CSS to Image app: Update Template



```
PUT https://connect.mindcloud.co/v1/universal/hTMLCSSToImageApp/latest/actions/update-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HTML/CSS to Image app `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/hTMLCSSToImageApp/latest/actions/update-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "templateId": "string",
  "html": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hTMLCSSToImageApp/latest/actions/update-template', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "templateId": "string",
    "html": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `templateId` | string | yes | Identifier of the template to update. |
| `html` | string | yes | Updated HTML markup for the template. |
| `css` | string | no | Updated CSS styles for the template. |
| `name` | string | no | Updated template name. |
| `description` | string | no | Updated template description. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "templateId": "string",
      "templateVersion": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `templateId` | string |  |
| `templateVersion` | number |  |

## Native endpoint

Through the native HTML/CSS to Image app API, this operation is `POST /v1/template/:templateId` (base URL `https://hcti.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-template.md) for the provider-specific parameters and requirements.

