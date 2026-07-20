# Webshipper: Create Return Cause

Creates a return cause in Webshipper.

```
POST https://connect.mindcloud.co/v1/universal/webshipper/latest/actions/create-return-cause
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Webshipper `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/webshipper/latest/actions/create-return-cause" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "data.type": "return_causes",
  "data.relationships.portal.data.type": "return_portals"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/webshipper/latest/actions/create-return-cause', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "data.type": "return_causes",
    "data.relationships.portal.data.type": "return_portals"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `data.attributes.description` | string | no | Description of the return cause. |
| `data.attributes.limitRefundMethods` | string | no | Whether refund methods should be limited. |
| `data.attributes.name` | string | no | Name of the return cause. |
| `data.attributes.requireComment` | string | no | Whether a comment is required for this return cause. |
| `data.attributes.supportImageRequired` | string | no | Whether a support image is required. |
| `data.relationships.portal.data.id` | string | no | Return portal ID. |
| `data.type` | string | yes | Use the default value `return_causes`. Default: `return_causes`. |
| `data.relationships.portal.data.type` | string | yes | Use the default value `return_portals`. Default: `return_portals`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "id": "string",
      "limit_refund_methods": true,
      "name": "Ava Chen",
      "require_comment": true,
      "support_image_required": true,
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `id` | string |  |
| `limit_refund_methods` | boolean |  |
| `name` | string |  |
| `require_comment` | boolean |  |
| `support_image_required` | boolean |  |
| `type` | string |  |

## Native endpoint

Through the native Webshipper API, this operation is `POST /return_causes` (base URL `https://{{credentials.accountName}}.api.webshipper.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-return-cause.md) for the provider-specific parameters and requirements.

