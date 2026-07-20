# Zixflow: Create Custom Attribute

Creates a new custom attribute in Zixflow.

```
POST https://connect.mindcloud.co/v1/universal/zixflow/latest/actions/create-custom-attribute
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zixflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zixflow/latest/actions/create-custom-attribute" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "target": "string",
  "targetId": "string",
  "apiKeyName": "Ava Chen",
  "inputType": "string",
  "name": "Ava Chen",
  "config": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zixflow/latest/actions/create-custom-attribute', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "target": "string",
    "targetId": "string",
    "apiKeyName": "Ava Chen",
    "inputType": "string",
    "name": "Ava Chen",
    "config": {}
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
| `apiKeyName` | string | yes | Attribute API key name. |
| `inputType` | string | yes | Attribute input type. |
| `name` | string | yes | Attribute display name. |
| `config` | object | yes | Attribute configuration object. |
| `defaultValue` | string | no | Default value for the attribute. |
| `description` | string | no | Attribute description. |
| `isEditable` | boolean | no | Whether the attribute is editable. |
| `isMultiSelect` | boolean | no | Whether multiple values can be selected. |
| `isRequired` | boolean | no | Whether the attribute is required. |
| `isUnique` | boolean | no | Whether the attribute must be unique. |
| `validation` | string | no | Validation mode. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
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
| `data` | object | Created attribute payload returned by Zixflow. |
| `message` | string | Provider success or error message. |
| `status` | boolean | Whether the attribute create request succeeded. |

## Native endpoint

Through the native Zixflow API, this operation is `POST /attributes/:target/:targetId` (base URL `https://api.zixflow.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-custom-attribute.md) for the provider-specific parameters and requirements.

