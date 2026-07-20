# OpenSea: Get Trending Collections

Retrieves trending collections from OpenSea.

```
GET https://connect.mindcloud.co/v1/universal/openSea/latest/actions/get-trending-collections
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OpenSea `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openSea/latest/actions/get-trending-collections?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openSea/latest/actions/get-trending-collections?${params}`, {
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
| `timeframe` | string | no | Time window for trending calculation. Options: one_minute, five_minutes, fifteen_minutes, one_hour, one_day, seven_days, thirty_days, one_year, all_time. |
| `chains[]` | array<string> | no | Blockchain(s) to filter by. Comma-separated list of chain identifiers. Unsupported chains are silently ignored; a 400 is returned only if all specified chains are unsupported. Accepts multiple values in one string, delimited by `,`. |
| `category` | string | no | Category to filter by (e.g. art, gaming, memberships, music, pfps, photography, domain-names, virtual-worlds, sports-collectibles). |
| `limit` | number | no | Maximum number of collections to return (1-100). |
| `cursor` | string | no | Cursor for pagination. Use the 'next' value from a previous response. |

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

Through the native OpenSea API, this operation is `GET /api/v2/collections/trending` (base URL `https://api.opensea.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-trending-collections.md) for the provider-specific parameters and requirements.

