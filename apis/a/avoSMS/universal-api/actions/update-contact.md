# AvoSMS: Update Contact

Updates an existing contact in AvoSMS.

```
PUT https://connect.mindcloud.co/v1/universal/avoSMS/latest/actions/update-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AvoSMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/avoSMS/latest/actions/update-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "listContactId": "69cc2daf52244",
  "contactTelephoneNumber": "33612345678"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/avoSMS/latest/actions/update-contact', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "listContactId": "69cc2daf52244",
    "contactTelephoneNumber": "33612345678"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `listContactId` | string | yes | Contact list ID Example: `69cc2daf52244`. |
| `contactTelephoneNumber` | string | yes | Contact phone number Example: `33612345678`. |
| `contactCivility` | string | no | Civility of the contact Example: `Ms`. |
| `contactName` | string | no | Contact last name Example: `Doe`. |
| `contactFirstName` | string | no | Contact first name Example: `Janet`. |
| `contactEmail` | string | no | Contact email address Example: `janet.doe@example.com`. |
| `contactBirthday` | string | no | Contact birthday Example: `1990-01-31`. |
| `contactOther` | string | no | Other contact information Example: `MindCloud Updated`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native AvoSMS API returns.

## Native endpoint

Through the native AvoSMS API, this operation is `POST /v1/contact/update` (base URL `https://api.avosms.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-contact.md) for the provider-specific parameters and requirements.

