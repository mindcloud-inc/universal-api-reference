# Zoho Writer: Merge And Email

Merges a document and emails it in Zoho Writer.

```
POST https://connect.mindcloud.co/v1/universal/zohoWriter/latest/actions/merge-and-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Writer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoWriter/latest/actions/merge-and-email" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "documentId": "string",
  "subject": "string",
  "recipientEmail": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoWriter/latest/actions/merge-and-email', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "documentId": "string",
    "subject": "string",
    "recipientEmail": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `documentId` | string | yes | The unique ID of the Zoho Writer document. |
| `subject` | string | yes | Email subject for the merge email. |
| `recipientEmail` | string | yes | Recipient email address for the inline merge email. |
| `mergeData` | string | no | JSON string for merge_data, for example {"data":[{...}]}. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "records": [
        {
          "email": "ava@example.com",
          "name": "Ava Chen",
          "status": "string"
        }
      ],
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `records` | array<object> |  |
| `records[].email` | string |  |
| `records[].name` | string |  |
| `records[].status` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Zoho Writer API, this operation is `POST /v1/documents/:document_id/merge/email` (base URL `{{credentials.accessTokenRequest.api_domain}}/writer/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/merge-and-email.md) for the provider-specific parameters and requirements.

