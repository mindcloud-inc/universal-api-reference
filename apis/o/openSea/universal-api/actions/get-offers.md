# OpenSea: Get Item Offers



```
GET https://connect.mindcloud.co/v1/universal/openSea/latest/actions/get-offers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OpenSea `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openSea/latest/actions/get-offers?connectionId=$CONNECTION_ID&chain=string&protocol=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "chain": "string",
  "protocol": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openSea/latest/actions/get-offers?${params}`, {
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
| `chainChain` | string | no | The blockchain on which to filter the results |
| `protocol` | string | yes | Protocol name (e.g. 'seaport') |
| `assetContractAddress` | string | no |  |
| `tokenIds[]` | array<string> | no | Accepts multiple values in one string, delimited by `,`. |
| `tokenIds[]` | array<string> | no | Accepts multiple values in one string, delimited by `,`. |
| `maker` | string | no |  |
| `orderDirection` | string | no |  |
| `orderBy` | string | no |  |
| `listedBefore` | string | no |  |
| `listedAfter` | string | no |  |
| `paymentTokenAddress` | string | no |  |
| `limit` | number | no | Number of items to return per page |
| `cursorValue` | string | no |  |

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

Through the native OpenSea API, this operation is `GET /api/v2/orders/{chain}/{protocol}/offers` (base URL `https://api.opensea.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-offers.md) for the provider-specific parameters and requirements.

