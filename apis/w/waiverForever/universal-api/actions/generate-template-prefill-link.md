# WaiverForever: Generate Template Prefill Link

Creates a prefilled template link in WaiverForever.

```
POST https://connect.mindcloud.co/v1/universal/waiverForever/latest/actions/generate-template-prefill-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WaiverForever `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/waiverForever/latest/actions/generate-template-prefill-link" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fields": "[object Object]",
  "templateId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/waiverForever/latest/actions/generate-template-prefill-link', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fields": "[object Object]",
    "templateId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `expireAt` | number | no | Expiration timestamp for the generated prefill link. Example: `1720749890`. |
| `fields` | object | yes | Prefilled field values that must match the template prefill schema for the template. Example: `[object Object]`. |
| `templateId` | string | yes | WaiverForever template identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "expireAt": 1,
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `expireAt` | number | Expiration timestamp for the prefill link. |
| `url` | string | Generated prefill signing URL. |

## Native endpoint

Through the native WaiverForever API, this operation is `POST /openapi/v2/template/:template_id/prefill` (base URL `https://api.waiverforever.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-template-prefill-link.md) for the provider-specific parameters and requirements.

