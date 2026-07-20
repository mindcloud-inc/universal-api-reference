# Nutshell: Create Contact

Creates a new contact in Nutshell.

```
POST https://connect.mindcloud.co/v1/universal/nutshell/latest/actions/create-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nutshell `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/nutshell/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/nutshell/latest/actions/create-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contacts[].name` | string | no | Full name for the contact. |
| `contacts[].description` | string | no | Description to show under the contact name. |
| `contacts[].emails[].value` | string | no | Email address for the contact. |
| `contacts[].phones[].value.countryCode` | string | no | Country code for the contact phone number. |
| `contacts[].phones[].value.number` | string | no | Phone number digits for the contact. |
| `contacts[].links.accounts[]` | array<string> | no | Company IDs to associate with the contact. Accepts multiple values as an array. |
| `contacts[].links.owner` | string | no | Owner user ID for the contact. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Nutshell API returns.

## Native endpoint

Through the native Nutshell API, this operation is `POST /contacts` (base URL `https://app.nutshell.com/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contact.md) for the provider-specific parameters and requirements.

