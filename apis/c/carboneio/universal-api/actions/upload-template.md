# Carbone.io: Upload Template

Creates a template in Carbone.io.

```
POST https://connect.mindcloud.co/v1/universal/carboneio/latest/actions/upload-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Carbone.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/carboneio/latest/actions/upload-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "template": "VGhpcyBpcyBhIGJhc2U2NC1lbmNvZGVkIHRlbXBsYXRlLi4u"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/carboneio/latest/actions/upload-template', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "template": "VGhpcyBpcyBhIGJhc2U2NC1lbmNvZGVkIHRlbXBsYXRlLi4u"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `category` | string | no | Category used to organize the template. |
| `comment` | string | no | Template comment. |
| `id` | string | no | Existing Template ID (64-bit) to append a new version to. Leave blank to create a new template ID. |
| `name` | string | no | Template name. |
| `tags[]` | array<string> | no | List of tags to assign to the template. |
| `template` | string | yes | Base64-encoded contents of the template file. Example: `VGhpcyBpcyBhIGJhc2U2NC1lbmNvZGVkIHRlbXBsYXRlLi4u`. |
| `versioning` | boolean | no | Enable template versioning for the uploaded template. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `deployedAt` | number | no | UTC Unix timestamp that marks the deployed template version. |
| `expireAt` | number | no | UTC Unix timestamp after which the template is deleted. |
| `sample[]` | array<object> | no | Sample data used in Carbone Studio for testing and development. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": 1,
      "id": "string",
      "size": 1,
      "templateId": "string",
      "type": "string",
      "versionId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | number | UTC Unix timestamp when the version was created. |
| `id` | string | Template ID returned when versioning metadata is included. |
| `size` | number | Uploaded template size in bytes. |
| `templateId` | string | Backward-compatible template identifier returned when versioning is disabled. |
| `type` | string | Uploaded template file type. |
| `versionId` | string | Version ID returned when versioning metadata is included. |

## Native endpoint

Through the native Carbone.io API, this operation is `POST /template` (base URL `https://api.carbone.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-template.md) for the provider-specific parameters and requirements.

