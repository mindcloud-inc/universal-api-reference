# PlumDocs: Generate Document

Generates a document from a PlumDocs workflow.

```
POST https://connect.mindcloud.co/v1/universal/plumDocs/latest/actions/generate-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PlumDocs `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/plumDocs/latest/actions/generate-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "wf_abc123"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/plumDocs/latest/actions/generate-document', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "wf_abc123"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The PlumDocs workflow id. Example: `wf_abc123`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "document": {},
      "id": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Workflow data echoed by PlumDocs |
| `document` | object | Generated document metadata |
| `id` | string | Document run id |
| `status` | string | Run status |

## Native endpoint

Through the native PlumDocs API, this operation is `POST /workflows/:id/run` (base URL `https://plumdocs.com/api/zapier`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-document.md) for the provider-specific parameters and requirements.

