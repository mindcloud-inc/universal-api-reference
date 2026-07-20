# DocuPotion: Create PNG Base64



```
POST https://connect.mindcloud.co/v1/universal/docuPotion/latest/actions/create-png-base64
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DocuPotion `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/docuPotion/latest/actions/create-png-base64" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "templateId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/docuPotion/latest/actions/create-png-base64', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "templateId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `templateId` | list<string> | yes | Choose the DocuPotion template to render. |
| `data` | object | no | Dynamic data that matches the variables in your template. Example: `[object Object]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "base64": "string",
      "format": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `base64` | string | Base64-encoded PNG content. |
| `format` | string | The generated file format. |
| `success` | boolean | Whether the request succeeded. |

## Native endpoint

Through the native DocuPotion API, this operation is `POST /v1/create` (base URL `https://api.docupotion.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-png-base64.md) for the provider-specific parameters and requirements.

