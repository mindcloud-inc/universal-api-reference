# GoDaddy CRM: Get DNS Records

Retrieves DNS records for a GoDaddy domain.

```
GET https://connect.mindcloud.co/v1/universal/goDaddyCRM/latest/actions/get-dns-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoDaddy CRM `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goDaddyCRM/latest/actions/get-dns-records?connectionId=$CONNECTION_ID&limit=25&offset=0&domain=example.com&type=A&name=%40" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "domain": "example.com",
  "type": "A",
  "name": "@"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goDaddyCRM/latest/actions/get-dns-records?${params}`, {
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
| `domain` | string | yes | Required domain whose DNS records should be retrieved Example: `example.com`. |
| `type` | string | yes | Required DNS record type Default: `A`. Example: `A`. |
| `name` | string | yes | Required DNS record name Default: `@`. Example: `@`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native GoDaddy CRM API returns.

## Native endpoint

Through the native GoDaddy CRM API, this operation is `GET /v1/domains/:domain/records/:type/:name` (base URL `https://api.godaddy.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-dns-records.md) for the provider-specific parameters and requirements.

