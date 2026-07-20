# Zixflow: Update Custom Attribute

Updates an existing custom attribute in Zixflow.

```
PUT https://connect.mindcloud.co/v1/universal/zixflow/latest/actions/update-custom-attribute
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zixflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/zixflow/latest/actions/update-custom-attribute" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "target": "string",
  "targetId": "string",
  "attributeId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zixflow/latest/actions/update-custom-attribute', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "target": "string",
    "targetId": "string",
    "attributeId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `target` | string | yes | Target resource type for attributes. |
| `targetId` | string | yes | Target resource identifier for attributes. |
| `attributeId` | string | yes | Attribute identifier. |
| `apiKeyName` | string | no | Attribute API key name. |
| `inputType` | string | no | Attribute input type. |
| `name` | string | no | Attribute display name. |
| `config` | object | no | Attribute configuration object. |
| `defaultValue` | string | no | Default value for the attribute. |
| `description` | string | no | Attribute description. |
| `isEditable` | boolean | no |  |
| `isMultiSelect` | boolean | no |  |
| `isRequired` | boolean | no |  |
| `isUnique` | boolean | no |  |
| `validation` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "status": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Provider success or error message. |
| `status` | boolean | Whether the attribute update request succeeded. |

## Native endpoint

Through the native Zixflow API, this operation is `PATCH /attributes/:target/:targetId/:attributeId` (base URL `https://api.zixflow.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-custom-attribute.md) for the provider-specific parameters and requirements.

