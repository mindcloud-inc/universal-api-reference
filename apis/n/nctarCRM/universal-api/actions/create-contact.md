# Néctar CRM: Create Contact

Creates a new contact in Néctar CRM.

```
POST https://connect.mindcloud.co/v1/universal/nctarCRM/latest/actions/create-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Néctar CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/nctarCRM/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "contactType": "3"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/nctarCRM/latest/actions/create-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "contactType": "3"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Contact name. |
| `contactType` | number | yes | Contact type: 0 client, 1 prospect, 2 suspect, 3 lead, 5 discarded. Default: `3`. |
| `emails[]` | array<string> | no | Email addresses for the contact. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Néctar CRM API returns.

## Native endpoint

Through the native Néctar CRM API, this operation is `POST /contatos/` (base URL `https://app.nectarcrm.com.br/crm/api/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contact.md) for the provider-specific parameters and requirements.

