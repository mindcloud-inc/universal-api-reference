# OpenSea: Get Events By NFT

Retrieves events for an NFT in OpenSea.

```
GET https://connect.mindcloud.co/v1/universal/openSea/latest/actions/list-events-by-nft
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OpenSea `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openSea/latest/actions/list-events-by-nft?connectionId=$CONNECTION_ID&chain=string&address=string&identifier=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "chain": "string",
  "address": "string",
  "identifier": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openSea/latest/actions/list-events-by-nft?${params}`, {
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
| `chain` | string | yes | The blockchain on which to filter the results |
| `address` | string | yes | The unique public blockchain identifier for the contract |
| `identifier` | string | yes | The NFT token id |
| `after` | number | no | Only show events after this timestamp (Unix timestamp in seconds) |
| `before` | number | no | Only show events before this timestamp (Unix timestamp in seconds) |
| `eventType[]` | array<string> | no | Filter by event types. To get order invalidation and revalidation events, please use the Stream API. The order status can also be checked on the Get Order endpoint. Accepts multiple values in one string, delimited by `,`. |
| `limit` | number | no | Number of items to return per page |
| `nextValue` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | object |  |

## Native endpoint

Through the native OpenSea API, this operation is `GET /api/v2/events/chain/{chain}/contract/{address}/nfts/{identifier}` (base URL `https://api.opensea.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-events-by-nft.md) for the provider-specific parameters and requirements.

