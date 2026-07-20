# Layer4: Create Token

Creates a new token in a Layer4 bucket.

```
POST https://connect.mindcloud.co/v1/universal/layer4/latest/actions/create-token
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Layer4 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/layer4/latest/actions/create-token" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "bucketId": "string",
  "supply": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/layer4/latest/actions/create-token', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "bucketId": "string",
    "supply": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `bucketId` | string | yes | Layer4 bucket ID. |
| `metadata` | object | no | Optional token metadata object. |
| `segmentId` | string | no | Optional segment ID. |
| `supply` | string | yes | Initial token supply. |
| `toAddress` | string | no | Optional recipient address or email. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bucketId": "string",
      "chain": "string",
      "contractId": "string",
      "image": {},
      "metadata": {},
      "metadataUri": "string",
      "segmentId": "string",
      "supply": "string",
      "tokenId": "string",
      "transactionHashes": [
        "string"
      ]
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
| `contractId` | string |  |
| `image` | object |  |
| `metadata` | object |  |
| `metadataUri` | string |  |
| `segmentId` | string |  |
| `supply` | string |  |
| `tokenId` | string |  |
| `transactionHashes` | array<string> |  |

## Native endpoint

Through the native Layer4 API, this operation is `POST /api/v1/buckets/:bucketId/tokens` (base URL `https://www.layer4.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-token.md) for the provider-specific parameters and requirements.

