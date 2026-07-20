# Shorten.REST: List Aliases by Domain

Retrieves aliases from Shorten.REST for a specific domain.

```
GET https://connect.mindcloud.co/v1/universal/shortenREST/latest/actions/list-aliases-by-domain
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shorten.REST `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shortenREST/latest/actions/list-aliases-by-domain?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shortenREST/latest/actions/list-aliases-by-domain?${params}`, {
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
| `domainName` | string | no | The domain name to get aliases for, without http/https or trailing slash. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "aliasName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `aliasName` | string | Alias name returned from the mapped aliases list. |

## Native endpoint

Through the native Shorten.REST API, this operation is `GET /aliases/all` (base URL `https://api.shorten.rest`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-aliases-by-domain.md) for the provider-specific parameters and requirements.

