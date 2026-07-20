# OpenSea: Get Trending Tokens

Retrieves trending tokens from OpenSea.

```
GET https://connect.mindcloud.co/v1/universal/openSea/latest/actions/get-trending-tokens
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OpenSea `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openSea/latest/actions/get-trending-tokens?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openSea/latest/actions/get-trending-tokens?${params}`, {
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
| `limit` | number | no | Number of results to return (default: 20, max: 100) |
| `chains[]` | array<string> | no | Filter by blockchain(s) Accepts multiple values in one string, delimited by `,`. |
| `chains[]` | array<string> | no | Filter by blockchain(s) Accepts multiple values in one string, delimited by `,`. |
| `cursor` | string | no | Pagination cursor for next page |

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

Through the native OpenSea API, this operation is `GET /api/v2/tokens/trending` (base URL `https://api.opensea.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-trending-tokens.md) for the provider-specific parameters and requirements.

