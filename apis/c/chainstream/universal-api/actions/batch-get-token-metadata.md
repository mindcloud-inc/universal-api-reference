# Chainstream: Batch Get Token Metadata

Retrieves token metadata in bulk from Chainstream.

```
GET https://connect.mindcloud.co/v1/universal/chainstream/latest/actions/batch-get-token-metadata
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chainstream `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chainstream/latest/actions/batch-get-token-metadata?connectionId=$CONNECTION_ID&chain=string&tokenAddresses=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "chain": "string",
  "tokenAddresses": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chainstream/latest/actions/batch-get-token-metadata?${params}`, {
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
| `chain` | string | yes | Supported blockchain chain |
| `tokenAddresses` | string | yes | Comma-separated list of token addresses |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Chainstream API returns.

## Native endpoint

Through the native Chainstream API, this operation is `GET /v2/token/:chain/metadata/multi` (base URL `https://api.chainstream.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/batch-get-token-metadata.md) for the provider-specific parameters and requirements.

