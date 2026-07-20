# Customers.ai: Update Contact

Updates an existing contact in Customers.ai.

```
PUT https://connect.mindcloud.co/v1/universal/customersai/latest/actions/update-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Customers.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/customersai/latest/actions/update-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "recipientId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/customersai/latest/actions/update-contact', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "recipientId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `recipientId` | string | yes | Recipient ID or contact ID of the contact to update. |
| `email` | string | no | Updated email address for the contact. |
| `attribute1` | string | no | Optional sample custom attribute value. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contactId": 1,
      "recipientId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contactId` | number | Updated contact ID. |
| `recipientId` | string | Recipient ID for the updated contact. |

## Native endpoint

Through the native Customers.ai API, this operation is `PUT /contacts/:recipient_id` (base URL `https://api.mobilemonkey.com/public`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-contact.md) for the provider-specific parameters and requirements.

