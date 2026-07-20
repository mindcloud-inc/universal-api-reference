# GoDaddy CRM: Add DNS Records

Adds DNS records to a GoDaddy domain.

```
PUT https://connect.mindcloud.co/v1/universal/goDaddyCRM/latest/actions/add-dns-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoDaddy CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/goDaddyCRM/latest/actions/add-dns-records" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "domain": "example.com",
  "records[].type": "A",
  "records[].name": "@",
  "records[].data": "203.0.113.10"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/goDaddyCRM/latest/actions/add-dns-records', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "domain": "example.com",
    "records[].type": "A",
    "records[].name": "@",
    "records[].data": "203.0.113.10"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `domain` | string | yes | Required domain whose DNS records should be augmented Example: `example.com`. |
| `records[].type` | string | yes | Required DNS record type Default: `A`. Example: `A`. |
| `records[].name` | string | yes | Required DNS record name Default: `@`. Example: `@`. |
| `records[].data` | string | yes | Required DNS record data Example: `203.0.113.10`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native GoDaddy CRM API returns.

## Native endpoint

Through the native GoDaddy CRM API, this operation is `PATCH /v1/domains/:domain/records` (base URL `https://api.godaddy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-dns-records.md) for the provider-specific parameters and requirements.

