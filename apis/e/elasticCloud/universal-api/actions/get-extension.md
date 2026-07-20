# Elastic Cloud: Get Extension

Retrieves an extension from Elastic Cloud.

```
GET https://connect.mindcloud.co/v1/universal/elasticCloud/latest/actions/get-extension
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Elastic Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/elasticCloud/latest/actions/get-extension?connectionId=$CONNECTION_ID&extensionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "extensionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/elasticCloud/latest/actions/get-extension?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `extensionId` | string | yes | Identifier for the extension. |
| `includeDeployments` | boolean | no | Include deployments that reference this extension. |

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

Through the native Elastic Cloud API, this operation is `GET /deployments/extensions/:extension_id` (base URL `https://api.elastic-cloud.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-extension.md) for the provider-specific parameters and requirements.

