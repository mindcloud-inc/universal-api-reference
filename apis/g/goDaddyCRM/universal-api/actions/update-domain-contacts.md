# GoDaddy CRM: Update Domain Contacts

Updates contacts for a GoDaddy domain.

```
PUT https://connect.mindcloud.co/v1/universal/goDaddyCRM/latest/actions/update-domain-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoDaddy CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/goDaddyCRM/latest/actions/update-domain-contacts" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customerId": "1234567890",
  "domain": "example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/goDaddyCRM/latest/actions/update-domain-contacts', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customerId": "1234567890",
    "domain": "example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customerId` | string | yes | Required customer identifier who owns the domain Example: `1234567890`. |
| `domain` | string | yes | Required domain whose contacts should be updated Example: `example.com`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `identityDocumentId` | string | no | Optional identity document associated with the registrant update Example: `doc-123`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native GoDaddy CRM API returns.

## Native endpoint

Through the native GoDaddy CRM API, this operation is `PATCH /v2/customers/:customerId/domains/:domain/contacts` (base URL `https://api.godaddy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-domain-contacts.md) for the provider-specific parameters and requirements.

