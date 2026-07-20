# CraftMyPDF: Create a PDF asynchronously

Creates a PDF asynchronously in CraftMyPDF.

```
POST https://connect.mindcloud.co/v1/universal/craftMyPDF/latest/actions/create-apdf-asynchronously
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CraftMyPDF `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/craftMyPDF/latest/actions/create-apdf-asynchronously" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "data": {},
  "templateId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/craftMyPDF/latest/actions/create-apdf-asynchronously', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "data": {},
    "templateId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `data` | object | yes |  |
| `templateId` | string | yes |  |
| `version` | string | no |  |
| `expiration` | number | no |  |
| `webhookUrl` | string | no |  |
| `imageResampleRes` | number | no |  |
| `cloudStorage` | number | no |  |
| `postactionS3Filekey` | string | no |  |
| `postactionS3Bucket` | string | no |  |
| `resizeImages` | boolean | no |  |
| `resizeMaxWidth` | number | no |  |
| `resizeMaxHeight` | number | no |  |
| `resizeFormat` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "isAsync": true,
      "status": "string",
      "transactionRef": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `isAsync` | boolean |  |
| `status` | string |  |
| `transactionRef` | string |  |

## Native endpoint

Through the native CraftMyPDF API, this operation is `POST /create-async` (base URL `https://api.craftmypdf.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-apdf-asynchronously.md) for the provider-specific parameters and requirements.

