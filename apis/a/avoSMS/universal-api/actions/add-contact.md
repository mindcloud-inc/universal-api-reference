# AvoSMS: Add Contact

Creates a new contact in AvoSMS.

```
POST https://connect.mindcloud.co/v1/universal/avoSMS/latest/actions/add-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AvoSMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/avoSMS/latest/actions/add-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "listContactId": "12345",
  "contactTelephoneNumber": "33612345678"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/avoSMS/latest/actions/add-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "listContactId": "12345",
    "contactTelephoneNumber": "33612345678"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `listContactId` | string | yes | Contact list ID Example: `12345`. |
| `contactTelephoneNumber` | string | yes | Contact phone number Example: `33612345678`. |
| `contactCivility` | string | no | Civility of the contact Example: `Mr`. |
| `contactName` | string | no | Contact last name Example: `Doe`. |
| `contactFirstName` | string | no | Contact first name Example: `Jane`. |
| `contactEmail` | string | no | Contact email address Example: `jane.doe@example.com`. |
| `contactBirthday` | string | no | Contact birthday Example: `1990-01-31`. |
| `contactOther` | string | no | Other contact information Example: `VIP`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native AvoSMS API returns.

## Native endpoint

Through the native AvoSMS API, this operation is `POST /v1/contact/add` (base URL `https://api.avosms.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-contact.md) for the provider-specific parameters and requirements.

