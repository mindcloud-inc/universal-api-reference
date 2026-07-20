# Paperless: Create Document With Hidden Blocks



```
POST https://connect.mindcloud.co/v1/universal/paperless/latest/actions/create-document-with-hidden-blocks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Paperless `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/paperless/latest/actions/create-document-with-hidden-blocks" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workspaceId": 1,
  "templateId": 1,
  "name": "Ava Chen",
  "blocks": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/paperless/latest/actions/create-document-with-hidden-blocks', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workspaceId": 1,
    "templateId": 1,
    "name": "Ava Chen",
    "blocks": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `workspaceId` | number | yes | The workspace where the new document will be created. |
| `templateId` | number | yes | The template to use as the blueprint for the new document. |
| `name` | string | yes | The name of the new document. |
| `blocks` | object | yes | Block visibility overrides keyed by template block slug. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "string",
      "id": 1,
      "name": "Ava Chen",
      "status": "string",
      "updated_at": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | string |  |
| `id` | number |  |
| `name` | string |  |
| `status` | string |  |
| `updated_at` | string |  |

## Native endpoint

Through the native Paperless API, this operation is `POST /documents` (base URL `https://app.paperless.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-document-with-hidden-blocks.md) for the provider-specific parameters and requirements.

