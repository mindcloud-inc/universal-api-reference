# Xodo Sign: Audit Log

Retrieves a document audit log from Xodo Sign.

```
GET https://connect.mindcloud.co/v1/universal/xodoSign/latest/actions/audit-log
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Xodo Sign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xodoSign/latest/actions/audit-log?connectionId=$CONNECTION_ID&documentHash=string&business_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "documentHash": "string",
  "business_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xodoSign/latest/actions/audit-log?${params}`, {
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
| `documentHash` | string | yes | The unique document hash to fetch the audit log for. |
| `business_id` | string | yes | The Xodo Sign business ID that owns the document. |

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
      "merged_document_file_checksum": "string",
      "signer_ip": "string",
      "time_stamp": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `client_ip` | string | Client IP address when available. |
| `combined_checksum` | string | Combined checksum based on event type, timestamp, and document checksum. |
| `document_checksum` | string | Data integrity value for the document. |
| `entry_id` | number | Unique database ID of the audit log entry. |
| `event_assoc_signer` | string | Signer number associated with the event when present. |
| `event_assoc_signer_additional_data` | object | Additional event metadata returned by Xodo Sign. |
| `event_assoc_signer_email` | string | Signer email associated with the event when present. |
| `event_assoc_signer_name` | string | Signer name associated with the event when present. |
| `event_type` | string | Event name identifier. |
| `merged_document_file_checksum` | string | Checksum of the signed document file when available. |
| `signer_ip` | string | Signer IP address when available. |
| `time_stamp` | number | Unix timestamp of the event. |

## Native endpoint

Through the native Xodo Sign API, this operation is `GET /document/:documentHash/audit_log` (base URL `https://api.eversign.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/audit-log.md) for the provider-specific parameters and requirements.

