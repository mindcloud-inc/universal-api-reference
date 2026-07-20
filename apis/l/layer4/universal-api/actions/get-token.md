# Layer4: Get Token

Retrieves a token from a Layer4 bucket.

```
GET https://connect.mindcloud.co/v1/universal/layer4/latest/actions/get-token
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Layer4 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/layer4/latest/actions/get-token?connectionId=$CONNECTION_ID&bucketId=string&tokenId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "bucketId": "string",
  "tokenId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/layer4/latest/actions/get-token?${params}`, {
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
| `tokenId` | string | yes | The Layer4 token identifier. |

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

Through the native Layer4 API, this operation is `GET /api/v1/buckets/:bucketId/tokens/:tokenId` (base URL `https://www.layer4.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-token.md) for the provider-specific parameters and requirements.

