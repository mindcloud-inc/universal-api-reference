# Host.io: List Domains by Backlink Target

Finds domains in Host.io by backlink target.

```
GET https://connect.mindcloud.co/v1/universal/hostio/latest/actions/list-domains-by-backlink-target
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Host.io `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hostio/latest/actions/list-domains-by-backlink-target?connectionId=$CONNECTION_ID&limit=25&offset=0&value=google.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "value": "google.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hostio/latest/actions/list-domains-by-backlink-target?${params}`, {
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
| `value` | string | yes | Domain that result domains link to from their homepage. Default: `google.com`. Example: `google.com`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "backlinks": "https://example.com",
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
| `backlinks` | string | Backlink target searched. |
| `domains` | array<string> | Domains linking to the target. |
| `page` | number | Current result page. |
| `total` | number | Total available result count. |

## Native endpoint

Through the native Host.io API, this operation is `GET /domains/backlinks/:value` (base URL `https://host.io/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-domains-by-backlink-target.md) for the provider-specific parameters and requirements.

