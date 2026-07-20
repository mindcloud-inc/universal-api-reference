# Documenso: Create Template

Creates a new template in Documenso.

```
POST https://connect.mindcloud.co/v1/universal/documenso/latest/actions/create-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Documenso `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/documenso/latest/actions/create-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "payload": {},
  "file": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/documenso/latest/actions/create-template', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "payload": {},
    "file": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `payload` | object | yes |  |
| `file` | file | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "envelopeId": "string",
      "id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `envelopeId` | string |  |
| `id` | number |  |

## Native endpoint

Through the native Documenso API, this operation is `POST /template/create` (base URL `https://app.documenso.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-template.md) for the provider-specific parameters and requirements.

