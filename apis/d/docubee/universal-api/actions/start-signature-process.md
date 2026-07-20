# Docubee: Start Signature Process

Starts a signature process in Docubee.

```
POST https://connect.mindcloud.co/v1/universal/docubee/latest/actions/start-signature-process
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Docubee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/docubee/latest/actions/start-signature-process" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/docubee/latest/actions/start-signature-process', {
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

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `body` | string | no | The signature process payload. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "documentId": "string",
      "processId": "string",
      "processName": "Ava Chen",
      "startedOn": "string",
      "status": "string",
      "testMode": true,
      "updatedOn": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `documentId` | string | The source document ID. |
| `processId` | string | The signature process ID. |
| `processName` | string | The signature process name. |
| `startedOn` | string | When the signature process started. |
| `status` | string | The signature process status. |
| `testMode` | boolean | Whether the signature process is running in test mode. |
| `updatedOn` | string | When the signature process was last updated. |

## Native endpoint

Through the native Docubee API, this operation is `POST /signatures` (base URL `https://docubee.app/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/start-signature-process.md) for the provider-specific parameters and requirements.

