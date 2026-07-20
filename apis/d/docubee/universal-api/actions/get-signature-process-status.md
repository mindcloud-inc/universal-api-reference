# Docubee: Get Signature Process Status

Retrieves the status of a Docubee signature process.

```
GET https://connect.mindcloud.co/v1/universal/docubee/latest/actions/get-signature-process-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Docubee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docubee/latest/actions/get-signature-process-status?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/docubee/latest/actions/get-signature-process-status?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `processId` | string | no | The signature process ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "documentId": "string",
      "processId": "string",
      "processName": "Ava Chen",
      "status": "string",
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
| `status` | string | The signature process status. |
| `updatedOn` | string | When the signature process was last updated. |

## Native endpoint

Through the native Docubee API, this operation is `GET /signatures/:processId/status` (base URL `https://docubee.app/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-signature-process-status.md) for the provider-specific parameters and requirements.

