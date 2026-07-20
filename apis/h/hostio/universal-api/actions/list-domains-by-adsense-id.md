# Host.io: List Domains by AdSense ID

Finds domains in Host.io by AdSense ID.

```
GET https://connect.mindcloud.co/v1/universal/hostio/latest/actions/list-domains-by-adsense-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Host.io `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hostio/latest/actions/list-domains-by-adsense-id?connectionId=$CONNECTION_ID&limit=25&offset=0&value=pub-1556223355139109" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "value": "pub-1556223355139109"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hostio/latest/actions/list-domains-by-adsense-id?${params}`, {
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
| `value` | string | yes | Google AdSense publisher ID to search for. Default: `pub-1556223355139109`. Example: `pub-1556223355139109`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "adsense": "string",
      "domains": [
        "string"
      ],
      "page": 1,
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `adsense` | string | AdSense publisher ID used for the lookup. |
| `domains` | array<string> | Domains associated with the AdSense publisher ID. |
| `page` | number | Current result page. |
| `total` | number | Total matching domains reported by Host.io. |

## Native endpoint

Through the native Host.io API, this operation is `GET /domains/adsense/:value` (base URL `https://host.io/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-domains-by-adsense-id.md) for the provider-specific parameters and requirements.

