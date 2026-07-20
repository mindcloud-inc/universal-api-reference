# Wati: Update Contact Attributes

Updates contact attributes for one contact in Wati.

```
PUT https://connect.mindcloud.co/v1/universal/wati/latest/actions/update-contact-attributes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wati `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/wati/latest/actions/update-contact-attributes" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "whatsappNumber": "string",
  "customParams[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/wati/latest/actions/update-contact-attributes', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "whatsappNumber": "string",
    "customParams[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `whatsappNumber` | string | yes | Target contact phone number. |
| `customParams[]` | array<object> | yes | Custom attributes to update on the contact. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | boolean | Whether Wati accepted the contact attribute update. |

## Native endpoint

Through the native Wati API, this operation is `POST /api/v1/updateContactAttributes/:whatsappNumber` (base URL `{{credentials.apiEndpointUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-contact-attributes.md) for the provider-specific parameters and requirements.

