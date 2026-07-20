# GoDaddy CRM: Replace Nameservers

Replaces nameservers for a GoDaddy domain.

```
PUT https://connect.mindcloud.co/v1/universal/goDaddyCRM/latest/actions/replace-nameservers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoDaddy CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/goDaddyCRM/latest/actions/replace-nameservers" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customerId": "1234567890",
  "domain": "example.com",
  "nameServers[]": "ns1.example.net"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/goDaddyCRM/latest/actions/replace-nameservers', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customerId": "1234567890",
    "domain": "example.com",
    "nameServers[]": "ns1.example.net"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customerId` | string | yes | Required customer identifier who owns the domain Example: `1234567890`. |
| `domain` | string | yes | Required domain whose nameservers should be replaced Example: `example.com`. |
| `nameServers[]` | string<string> | yes | Required list of replacement nameservers Accepts multiple values as an array. Example: `ns1.example.net`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native GoDaddy CRM API returns.

## Native endpoint

Through the native GoDaddy CRM API, this operation is `PUT /v2/customers/:customerId/domains/:domain/nameServers` (base URL `https://api.godaddy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/replace-nameservers.md) for the provider-specific parameters and requirements.

