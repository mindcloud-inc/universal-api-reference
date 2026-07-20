# GoDaddy CRM: Delete DNS Records By Type And Name

Deletes DNS records from a GoDaddy domain.

```
DELETE https://connect.mindcloud.co/v1/universal/goDaddyCRM/latest/actions/delete-dns-records-by-type-and-name
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoDaddy CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/goDaddyCRM/latest/actions/delete-dns-records-by-type-and-name?connectionId=$CONNECTION_ID&domain=example.com&type=A&name=%40" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "domain": "example.com",
  "type": "A",
  "name": "@"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goDaddyCRM/latest/actions/delete-dns-records-by-type-and-name?${params}`, {
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
| `domain` | string | yes | Required domain whose DNS records should be deleted Example: `example.com`. |
| `type` | string | yes | Required DNS record type to delete Default: `A`. Example: `A`. |
| `name` | string | yes | Required DNS record name to delete Default: `@`. Example: `@`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native GoDaddy CRM API returns.

## Native endpoint

Through the native GoDaddy CRM API, this operation is `DELETE /v1/domains/:domain/records/:type/:name` (base URL `https://api.godaddy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-dns-records-by-type-and-name.md) for the provider-specific parameters and requirements.

