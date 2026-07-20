# Docubee: List Signature Processes

Retrieves signature processes from Docubee.

```
GET https://connect.mindcloud.co/v1/universal/docubee/latest/actions/list-signature-processes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Docubee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docubee/latest/actions/list-signature-processes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/docubee/latest/actions/list-signature-processes?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



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

Through the native Docubee API, this operation is `GET /signatures` (base URL `https://docubee.app/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-signature-processes.md) for the provider-specific parameters and requirements.

