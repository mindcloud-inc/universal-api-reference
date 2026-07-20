# DatoCMS: Update Upload



```
PUT https://connect.mindcloud.co/v1/universal/datoCMS/latest/actions/update-upload
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DatoCMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/datoCMS/latest/actions/update-upload" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "uploadId": "string",
  "attributes": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/datoCMS/latest/actions/update-upload', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "uploadId": "string",
    "attributes": "[object Object]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `uploadId` | string | yes | Upload ID. |
| `attributes` | object | yes | Upload attributes payload. Example: `[object Object]`. |
| `attributes.tags[]` | array<string> | no |  |
| `attributes.author` | string | no |  |
| `attributes.basename` | string | no |  |
| `attributes.copyright` | string | no |  |
| `attributes.notes` | string | no |  |
| `attributes.path` | string | no |  |
| `attributes.defaultFieldMetadata` | object | no |  |
| `attributes.defaultFieldMetadata.en` | object | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `type` | string |  |

## Native endpoint

Through the native DatoCMS API, this operation is `PUT /uploads/:uploadId` (base URL `https://site-api.datocms.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-upload.md) for the provider-specific parameters and requirements.

