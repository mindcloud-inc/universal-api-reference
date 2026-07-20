# Elastic Cloud: Update Extension

Updates an existing extension in Elastic Cloud.

```
PUT https://connect.mindcloud.co/v1/universal/elasticCloud/latest/actions/update-extension
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Elastic Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/elasticCloud/latest/actions/update-extension" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "body": {},
  "extensionId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/elasticCloud/latest/actions/update-extension', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "body": {},
    "extensionId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `body` | object | yes | The extension update data. |
| `extensionId` | string | yes | Identifier for the extension. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "extensionType": "string",
      "fileMetadata": {
        "url": "https://example.com"
      },
      "id": "string",
      "name": "Ava Chen",
      "organizationId": "string",
      "url": "https://example.com",
      "version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `extensionType` | string |  |
| `fileMetadata.url` | string |  |
| `id` | string |  |
| `name` | string |  |
| `organizationId` | string |  |
| `url` | string |  |
| `version` | string |  |

## Native endpoint

Through the native Elastic Cloud API, this operation is `POST /deployments/extensions/:extension_id` (base URL `https://api.elastic-cloud.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-extension.md) for the provider-specific parameters and requirements.

