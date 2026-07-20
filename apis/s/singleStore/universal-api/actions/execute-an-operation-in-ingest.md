# SingleStore: Execute an Operation in Ingest

Executes an ingest operation in SingleStore.

```
POST https://connect.mindcloud.co/v1/universal/singleStore/latest/actions/execute-an-operation-in-ingest
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SingleStore `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/singleStore/latest/actions/execute-an-operation-in-ingest" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "operation": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/singleStore/latest/actions/execute-an-operation-in-ingest', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "operation": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `operation` | string | yes | Ingest operation to execute. The docs show full, syncnew, syncstruct, and delta. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Provider message describing the operation result. |
| `success` | boolean | Whether the ingest operation request succeeded. |

## Native endpoint

Through the native SingleStore API, this operation is `POST /ops/extract/{operation}` (base URL `https://{{credentials.flowEndpoint}}:30081/ingest/api/ingest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/execute-an-operation-in-ingest.md) for the provider-specific parameters and requirements.

