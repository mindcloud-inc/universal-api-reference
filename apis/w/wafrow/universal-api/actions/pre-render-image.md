# Wafrow: Pre-render Image

Creates a pre-rendered image or PDF in Wafrow.

```
POST https://connect.mindcloud.co/v1/universal/wafrow/latest/actions/pre-render-image
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wafrow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/wafrow/latest/actions/pre-render-image" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "templateId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/wafrow/latest/actions/pre-render-image', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "templateId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `templateId` | string | yes | The Wafrow template UUID to pre-render immediately. |
| `personalize` | object | no | Layer overrides keyed by template layer name. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Wafrow API returns.

## Native endpoint

Through the native Wafrow API, this operation is `POST /img/:template_id` (base URL `https://wafrow.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/pre-render-image.md) for the provider-specific parameters and requirements.

