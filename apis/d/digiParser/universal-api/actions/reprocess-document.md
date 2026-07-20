# DigiParser: Reprocess Document



```
PUT https://connect.mindcloud.co/v1/universal/digiParser/latest/actions/reprocess-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DigiParser `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/digiParser/latest/actions/reprocess-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "parserId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/digiParser/latest/actions/reprocess-document', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "parserId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `parserId` | string | yes | Parser UUID from DigiParser Parser Settings -> General Settings. |
| `documentId` | string | no | Existing document UUID to reprocess. |
| `externalId` | string | no | External ID of the document to reprocess for this parser. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "documentId": "string",
      "status": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `documentId` | string | Document UUID that was requeued for processing. |
| `status` | string | Current processing state after the reprocess request. |
| `success` | boolean | Whether the reprocess request was accepted. |

## Native endpoint

Through the native DigiParser API, this operation is `POST /api/v1/process/:parserId/reprocess` (base URL `https://app.digiparser.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/reprocess-document.md) for the provider-specific parameters and requirements.

