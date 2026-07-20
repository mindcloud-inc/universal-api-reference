# BigMailer: Update Contact

Updates an existing contact in a BigMailer brand.

```
PUT https://connect.mindcloud.co/v1/universal/bigMailer/latest/actions/update-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BigMailer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/bigMailer/latest/actions/update-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "brandId": "string",
  "contactId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bigMailer/latest/actions/update-contact', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "brandId": "string",
    "contactId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `brandId` | string | yes | ID of the brand containing the contact. |
| `contactId` | string | yes | ID or email address of the contact. |
| `fieldValuesOp` | string | no | How field values should be applied. Default: `replace`. |
| `listIdsOp` | string | no | How list IDs should be applied. Default: `replace`. |
| `unsubscribeIdsOp` | string | no | How unsubscribe IDs should be applied. Default: `replace`. |
| `email` | string | no | Email address of the contact. |
| `fieldValues[]` | array<object> | no | Field values to save with the contact. |
| `listIds[]` | array<string> | no | IDs of lists the contact should be added to. |
| `unsubscribeAll` | boolean | no | Unsubscribe the contact from all message types. |
| `unsubscribeIds[]` | array<string> | no | IDs of message types the contact should be unsubscribed from. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native BigMailer API returns.

## Native endpoint

Through the native BigMailer API, this operation is `POST /brands/:brand_id/contacts/:contact_id` (base URL `https://api.bigmailer.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-contact.md) for the provider-specific parameters and requirements.

