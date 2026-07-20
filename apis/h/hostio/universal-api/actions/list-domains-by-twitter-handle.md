# Host.io: List Domains by Twitter Handle

Finds domains in Host.io by Twitter handle.

```
GET https://connect.mindcloud.co/v1/universal/hostio/latest/actions/list-domains-by-twitter-handle
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Host.io `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hostio/latest/actions/list-domains-by-twitter-handle?connectionId=$CONNECTION_ID&limit=25&offset=0&value=elonmusk" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "value": "elonmusk"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hostio/latest/actions/list-domains-by-twitter-handle?${params}`, {
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
| `value` | string | yes | Twitter handle to search for. Default: `elonmusk`. Example: `elonmusk`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "domains": [
        "string"
      ],
      "page": 1,
      "total": 1,
      "twitter": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `domains` | array<string> | Domains associated with the Twitter handle. |
| `page` | number | Current result page. |
| `total` | number | Total matching domains reported by Host.io. |
| `twitter` | string | Twitter handle used for the lookup. |

## Native endpoint

Through the native Host.io API, this operation is `GET /domains/twitter/:value` (base URL `https://host.io/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-domains-by-twitter-handle.md) for the provider-specific parameters and requirements.

