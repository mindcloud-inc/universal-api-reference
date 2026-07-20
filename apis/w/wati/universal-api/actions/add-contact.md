# Wati: Add Contact

Creates a new contact in Wati.

```
POST https://connect.mindcloud.co/v1/universal/wati/latest/actions/add-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wati `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/wati/latest/actions/add-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "whatsappNumber": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/wati/latest/actions/add-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "whatsappNumber": "string",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `whatsappNumber` | string | yes | Target WhatsApp phone number for the contact. |
| `name` | string | yes | Display name for the contact. |
| `customParams[]` | array<object> | no | Custom attributes to store on the contact. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "info": "string",
      "result": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `info` | string | Provider message for the contact create attempt. |
| `result` | boolean | Whether Wati accepted the contact creation request. |

## Native endpoint

Through the native Wati API, this operation is `POST /api/v1/addContact/:whatsappNumber` (base URL `{{credentials.apiEndpointUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-contact.md) for the provider-specific parameters and requirements.

