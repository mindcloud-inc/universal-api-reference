# Layer4: Get Record

Retrieves a record from a Layer4 bucket.

```
GET https://connect.mindcloud.co/v1/universal/layer4/latest/actions/get-record
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Layer4 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/layer4/latest/actions/get-record?connectionId=$CONNECTION_ID&bucketId=string&recordId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "bucketId": "string",
  "recordId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/layer4/latest/actions/get-record?${params}`, {
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
| `bucketId` | string | yes | Layer4 bucket ID. |
| `decrypt` | boolean | no | Whether to decrypt the record. |
| `recordId` | string | yes | Layer4 record ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bucketId": "string",
      "chain": "string",
      "contentType": "string",
      "contractId": "string",
      "createdAt": "string",
      "data": "string",
      "files": [
        {}
      ],
      "isEncrypted": true,
      "recordId": "string",
      "segmentId": "string",
      "transactionHashes": [
        "string"
      ],
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bucketId` | string |  |
| `chain` | string |  |
| `contentType` | string |  |
| `contractId` | string |  |
| `createdAt` | string |  |
| `data` | string |  |
| `files` | array<object> |  |
| `isEncrypted` | boolean |  |
| `recordId` | string |  |
| `segmentId` | string |  |
| `transactionHashes` | array<string> |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Layer4 API, this operation is `GET /api/v1/buckets/:bucketId/records/:recordId` (base URL `https://www.layer4.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-record.md) for the provider-specific parameters and requirements.

