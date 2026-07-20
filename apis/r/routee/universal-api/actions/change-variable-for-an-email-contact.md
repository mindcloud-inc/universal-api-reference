# Routee: Change Variable for an Email Contact

Changes a variable for an email contact in Routee.

```
POST https://connect.mindcloud.co/v1/universal/routee/latest/actions/change-variable-for-an-email-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Routee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/routee/latest/actions/change-variable-for-an-email-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "addressBookId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/routee/latest/actions/change-variable-for-an-email-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "addressBookId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `addressBookId` | string | yes | ID of the address book containing the necessary email contact with the variable with “name” value |
| `email` | string | no | email contact, that will have the variable with “name” value changed to “John” |
| `variables[]` | array<object> | no | array with variables, which is defined by the parameters name (variable name) and value (variable value) |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Routee API returns.

## Native endpoint

Through the native Routee API, this operation is `POST /addressbooks/:addressBookId/emails/variable` (base URL `https://connect.routee.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/change-variable-for-an-email-contact.md) for the provider-specific parameters and requirements.

