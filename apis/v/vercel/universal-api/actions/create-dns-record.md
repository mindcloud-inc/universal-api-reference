# Vercel: Create DNS Record

Creates a DNS record in Vercel.

```
POST https://connect.mindcloud.co/v1/universal/vercel/latest/actions/create-dns-record
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vercel `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/vercel/latest/actions/create-dns-record" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "domain": "string",
  "name": "Ava Chen",
  "type": "string",
  "value": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/vercel/latest/actions/create-dns-record', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "domain": "string",
    "name": "Ava Chen",
    "type": "string",
    "value": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `domain` | string | yes | The domain name to create the DNS record under. |
| `name` | string | yes | The DNS record name. |
| `type` | string | yes | The DNS record type. |
| `value` | string | yes | The DNS record value. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Vercel API returns.

## Native endpoint

Through the native Vercel API, this operation is `POST /v2/domains/:domain/records` (base URL `https://api.vercel.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-dns-record.md) for the provider-specific parameters and requirements.

