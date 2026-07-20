# SignWell: Create Template

Creates a new template in SignWell.

```
POST https://connect.mindcloud.co/v1/universal/signWell/latest/actions/create-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SignWell `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/signWell/latest/actions/create-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "files[]": [
    {}
  ],
  "files[].name": "Ava Chen",
  "placeholders[]": [
    {}
  ],
  "placeholders[].id": "string",
  "placeholders[].name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/signWell/latest/actions/create-template', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "files[]": [{}],
    "files[].name": "Ava Chen",
    "placeholders[]": [{}],
    "placeholders[].id": "string",
    "placeholders[].name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | no |  |
| `test_mode` | boolean | no |  |
| `files[]` | array<object> | yes |  |
| `files[].name` | string | yes |  |
| `files[].file_url` | string | no | Public URL for the template file. Provide either File URL or File Base64, not both. |
| `files[].file_base64` | string | no | Base64-encoded file content for the template file. Provide either File URL or File Base64, not both. |
| `placeholders[]` | array<object> | yes |  |
| `placeholders[].id` | string | yes |  |
| `placeholders[].name` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native SignWell API returns.

## Native endpoint

Through the native SignWell API, this operation is `POST /document_templates` (base URL `https://www.signwell.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-template.md) for the provider-specific parameters and requirements.

