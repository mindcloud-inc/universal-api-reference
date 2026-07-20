# Documint: Merge Template

Creates a document from a template in Documint.

```
POST https://connect.mindcloud.co/v1/universal/documint/latest/actions/merge-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Documint `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/documint/latest/actions/merge-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "69bac297724eda8b0297192e"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/documint/latest/actions/merge-template', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "69bac297724eda8b0297192e"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The Documint template ID to merge. Example: `69bac297724eda8b0297192e`. |
| `ignoreFields` | string | no | Comma-separated template fields to ignore during merge. |
| `watchFields` | string | no | Fields to watch during merge preview/debugging. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_id": "string",
      "account": "string",
      "aws": {},
      "createdAt": "string",
      "dataHash": "string",
      "expiresAt": "string",
      "fileExtension": "string",
      "isLive": true,
      "isTest": true,
      "metadata": {},
      "name": "Ava Chen",
      "template": "string",
      "templateHash": "string",
      "updatedAt": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_id` | string |  |
| `account` | string |  |
| `aws` | object |  |
| `createdAt` | string |  |
| `dataHash` | string |  |
| `expiresAt` | string |  |
| `fileExtension` | string |  |
| `isLive` | boolean |  |
| `isTest` | boolean |  |
| `metadata` | object |  |
| `name` | string |  |
| `template` | string |  |
| `templateHash` | string |  |
| `updatedAt` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Documint API, this operation is `POST /templates/:id/content` (base URL `https://api.documint.me/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/merge-template.md) for the provider-specific parameters and requirements.

