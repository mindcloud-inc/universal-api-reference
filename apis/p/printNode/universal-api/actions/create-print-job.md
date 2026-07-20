# PrintNode: Create Print Job

Creates a new print job in PrintNode.

```
POST https://connect.mindcloud.co/v1/universal/printNode/latest/actions/create-print-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PrintNode `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/printNode/latest/actions/create-print-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "printerId": 1,
  "contentType": "string",
  "content": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/printNode/latest/actions/create-print-job', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "printerId": 1,
    "contentType": "string",
    "content": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `printerId` | number | yes | The ID of the printer you want to print to. |
| `contentType` | string | yes | One of pdf_uri, pdf_base64, raw_uri, or raw_base64. |
| `content` | string | yes | A document URI or a base64-encoded document, depending on contentType. |
| `title` | string | no | Optional print queue title. |
| `source` | string | no | Optional description of where the print job originated. |
| `options` | object | no | Optional object of PrintNode print options, such as copies, pages, duplex, paper, or bin. |
| `expireAfter` | number | no | Optional maximum number of seconds PrintNode should retain the print job before expiry. |
| `qty` | number | no | Optional number of times the print job should be delivered to the queue. |
| `authentication` | object | no | Optional HTTP Basic or Digest authentication object used when PrintNode must download the document from a protected URI. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "value": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `value` | number | ID of the created print job. |

## Native endpoint

Through the native PrintNode API, this operation is `POST /printjobs` (base URL `https://api.printnode.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-print-job.md) for the provider-specific parameters and requirements.

