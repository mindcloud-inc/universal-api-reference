# Layer4: List Records

Retrieves records from a Layer4 bucket.

```
GET https://connect.mindcloud.co/v1/universal/layer4/latest/actions/list-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Layer4 `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/layer4/latest/actions/list-records?connectionId=$CONNECTION_ID&limit=25&offset=0&bucketId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "bucketId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/layer4/latest/actions/list-records?${params}`, {
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
| `bucketId` | string | yes | The Layer4 bucket identifier. |
| `segmentId` | string | no | Filter records by segment. |
| `decrypt` | boolean | no | Return decrypted records when available. |

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

Through the native Layer4 API, this operation is `GET /api/v1/buckets/:bucketId/records` (base URL `https://www.layer4.app`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-records.md) for the provider-specific parameters and requirements.

