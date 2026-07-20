# Eversign: Audit Log

Retrieves a document audit log from Eversign.

```
GET https://connect.mindcloud.co/v1/universal/eversign/latest/actions/audit-log
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Eversign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eversign/latest/actions/audit-log?connectionId=$CONNECTION_ID&documentHash=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "documentHash": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eversign/latest/actions/audit-log?${params}`, {
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
| `documentHash` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "client_ip": "string",
      "combined_checksum": "string",
      "document_checksum": "string",
      "entry_id": 1,
      "event_assoc_signer": "string",
      "event_assoc_signer_additional_data": {},
      "event_assoc_signer_email": "ava@example.com",
      "event_assoc_signer_name": "Ava Chen",
      "event_type": "string",
      "is_exported": "string",
      "merged_document_file_checksum": "string",
      "signer_ip": "string",
      "time_stamp": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `client_ip` | string |  |
| `combined_checksum` | string |  |
| `document_checksum` | string |  |
| `entry_id` | number |  |
| `event_assoc_signer` | string |  |
| `event_assoc_signer_additional_data` | object |  |
| `event_assoc_signer_email` | string |  |
| `event_assoc_signer_name` | string |  |
| `event_type` | string |  |
| `is_exported` | string |  |
| `merged_document_file_checksum` | string |  |
| `signer_ip` | string |  |
| `time_stamp` | string |  |

## Native endpoint

Through the native Eversign API, this operation is `GET /document/:documentHash/audit_log` (base URL `https://api.eversign.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/audit-log.md) for the provider-specific parameters and requirements.

