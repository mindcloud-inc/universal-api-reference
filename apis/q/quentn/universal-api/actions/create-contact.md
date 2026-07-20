# Quentn: Create Contact



```
POST https://connect.mindcloud.co/v1/universal/quentn/latest/actions/create-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Quentn `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/quentn/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "name@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/quentn/latest/actions/create-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "name@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | yes | Valid email address for the new Quentn contact. Example: `name@example.com`. |
| `firstName` | string | no | Contact first name. Example: `Ada`. |
| `lastName` | string | no | Contact last name. Example: `Lovelace`. |
| `street` | string | no | Billing or street address. Example: `123 Market Street`. |
| `city` | string | no | City for the full-address fallback. Example: `Berlin`. |
| `postalCode` | string | no | Postal code for the full-address fallback. Example: `10115`. |
| `comment` | string | no | Optional comment to add while creating the contact. Example: `Imported from MindCloud`. |
| `requestIp` | string | no | IPv4 address associated with the contact submission. Required when flood protection options are used. Example: `203.0.113.10`. |
| `duplicateCheckMethod` | string | no | How Quentn should check for duplicates: auto, email, or none. Example: `auto`. |
| `duplicateMergeMethod` | string | no | How Quentn should merge duplicate contacts: update_add, update, or add. Example: `update_add`. |
| `floodLimit` | number | no | Maximum number of contacts allowed from the same request IP within an hour. Example: `5`. |
| `spamProtection` | boolean | no | Whether Quentn should check the request IP against a spam database. Example: `true`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | The id of the created Quentn contact. |

## Native endpoint

Through the native Quentn API, this operation is `POST /contact` (base URL `https://tbg6y3.us-1.quentn.com/public/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contact.md) for the provider-specific parameters and requirements.

