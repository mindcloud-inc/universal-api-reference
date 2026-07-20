# Modusign: Create Signature Request from Template

Creates a signature request from a template in Modusign.

```
POST https://connect.mindcloud.co/v1/universal/modusign/latest/actions/create-signature-request-from-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Modusign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/modusign/latest/actions/create-signature-request-from-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/modusign/latest/actions/create-signature-request-from-template', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "id": "string",
      "status": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string | The creation timestamp. |
| `id` | string | The created document ID. |
| `status` | string | The document status. |
| `updatedAt` | string | The update timestamp. |

## Native endpoint

Through the native Modusign API, this operation is `POST /documents/request-with-template` (base URL `https://api.modusign.co.kr`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-signature-request-from-template.md) for the provider-specific parameters and requirements.

