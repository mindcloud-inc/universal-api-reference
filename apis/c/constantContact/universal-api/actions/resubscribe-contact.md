# Constant Contact: Resubscribe Contact

Resubscribes a contact in Constant Contact.

```
PUT https://connect.mindcloud.co/v1/universal/constantContact/latest/actions/resubscribe-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Constant Contact `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/constantContact/latest/actions/resubscribe-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contactId": "string",
  "listIds[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/constantContact/latest/actions/resubscribe-contact', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contactId": "string",
    "listIds[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contactId` | string | yes | Unique ID of the contact to resubscribe. |
| `listIds[]` | array<string> | yes | List IDs to resubscribe the contact to (array of strings). |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contactId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contactId` | string |  |

## Native endpoint

Through the native Constant Contact API, this operation is `PUT /contacts/resubscribe/:contact_id` (base URL `https://api.cc.email/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/resubscribe-contact.md) for the provider-specific parameters and requirements.

