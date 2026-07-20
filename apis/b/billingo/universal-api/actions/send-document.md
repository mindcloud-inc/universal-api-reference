# Billingo: Send Document

Sends a document to email recipients in Billingo.

```
POST https://connect.mindcloud.co/v1/universal/billingo/latest/actions/send-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Billingo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/billingo/latest/actions/send-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "0"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/billingo/latest/actions/send-document', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "0"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | Billingo document ID to send. Default: `0`. |
| `emails[]` | array<string> | no | Email addresses to receive the document. Accepts multiple values as an array. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "emails": [
        "ava@example.com"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `emails` | array<string> | Email addresses where the document was sent. |

## Native endpoint

Through the native Billingo API, this operation is `POST /documents/:id/send` (base URL `https://api.billingo.hu/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-document.md) for the provider-specific parameters and requirements.

