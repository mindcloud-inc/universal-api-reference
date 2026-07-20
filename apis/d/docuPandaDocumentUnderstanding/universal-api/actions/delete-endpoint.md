# DocuPanda - Document Understanding: Deregister an Endpoint



```
POST https://connect.mindcloud.co/v1/universal/docuPandaDocumentUnderstanding/latest/actions/delete-endpoint
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DocuPanda - Document Understanding `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/docuPandaDocumentUnderstanding/latest/actions/delete-endpoint" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "endpointId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/docuPandaDocumentUnderstanding/latest/actions/delete-endpoint', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "endpointId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `endpointId` | string | yes | The ID which identifies the webhook endpoint |

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
| `success` | boolean | The webhook endpoint was successfully deleted |

## Native endpoint

Through the native DocuPanda - Document Understanding API, this operation is `POST /webhook/delete-endpoint` (base URL `https://app.docupipe.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-endpoint.md) for the provider-specific parameters and requirements.

