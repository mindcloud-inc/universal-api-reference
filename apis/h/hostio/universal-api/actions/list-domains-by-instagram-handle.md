# Host.io: List Domains by Instagram Handle

Finds domains in Host.io by Instagram handle.

```
GET https://connect.mindcloud.co/v1/universal/hostio/latest/actions/list-domains-by-instagram-handle
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Host.io `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hostio/latest/actions/list-domains-by-instagram-handle?connectionId=$CONNECTION_ID&limit=25&offset=0&value=nasa" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "value": "nasa"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hostio/latest/actions/list-domains-by-instagram-handle?${params}`, {
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
| `value` | string | yes | Instagram handle to search for. Default: `nasa`. Example: `nasa`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "domains": [
        "string"
      ],
      "instagram": "string",
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
| `domains` | array<string> | Domains associated with the Instagram handle. |
| `instagram` | string | Instagram handle used for the lookup. |
| `page` | number | Current result page. |
| `total` | number | Total matching domains reported by Host.io. |

## Native endpoint

Through the native Host.io API, this operation is `GET /domains/instagram/:value` (base URL `https://host.io/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-domains-by-instagram-handle.md) for the provider-specific parameters and requirements.

