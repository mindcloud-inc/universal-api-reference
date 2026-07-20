# Alegra: Create Contact

Creates a new contact in Alegra.

```
POST https://connect.mindcloud.co/v1/universal/alegra/latest/actions/create-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Alegra `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/alegra/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/alegra/latest/actions/create-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes |  |
| `identification` | string | no |  |
| `identificationObject.number` | string | no | Use for country-specific contact versions that require a structured identification object, such as Peru. |
| `identificationObject.type` | string | no | Use for country-specific contact versions that require a structured identification object, such as Peru. |
| `address.city` | string | no |  |
| `address.address` | string | no |  |
| `phonePrimary` | string | no |  |
| `phoneSecondary` | string | no |  |
| `mobile` | string | no |  |
| `seller` | string | no |  |
| `priceList` | string | no |  |
| `term` | string | no |  |
| `creditLimit` | number | no |  |
| `email` | string | no |  |
| `type` | string | no |  |
| `status` | string | no |  |
| `fax` | string | no |  |
| `accounting.debtToPay` | string | no |  |
| `accounting.accountReceivable` | string | no |  |
| `internalContacts[].name` | string | no |  |
| `internalContacts[].lastName` | string | no |  |
| `internalContacts[].email` | string | no |  |
| `internalContacts[].mobile` | string | no |  |
| `internalContacts[].phone` | string | no |  |
| `internalContacts[].sendNotifications` | string | no |  |
| `ignoreRepeated` | boolean | no |  |
| `statementAttached` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Alegra API returns.

## Native endpoint

Through the native Alegra API, this operation is `POST /contacts` (base URL `https://api.alegra.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contact.md) for the provider-specific parameters and requirements.

