# Carbone.io: Update Template

Updates a template in Carbone.io.

```
PUT https://connect.mindcloud.co/v1/universal/carboneio/latest/actions/update-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Carbone.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/carboneio/latest/actions/update-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "templateIdOrVersionId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/carboneio/latest/actions/update-template', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "templateIdOrVersionId": "string"
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
| `name` | string | no | Template name. |
| `tags[]` | array<string> | no | List of tags to assign to the template. |
| `templateIdOrVersionId` | string | yes | Template ID (64-bit) or Version ID (SHA-256) to update. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `deployedAt` | number | no | UTC Unix timestamp that marks the deployed template version. |
| `expireAt` | number | no | UTC Unix timestamp after which the template is deleted. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean | Whether the template metadata update succeeded. |

## Native endpoint

Through the native Carbone.io API, this operation is `PATCH /template/[:templateId-or-versionId]` (base URL `https://api.carbone.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-template.md) for the provider-specific parameters and requirements.

