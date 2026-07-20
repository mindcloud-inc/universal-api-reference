# CRM Messaging: Update Contact

Updates an existing contact in CRM Messaging.

```
PUT https://connect.mindcloud.co/v1/universal/cRMMessaging/latest/actions/update-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CRM Messaging `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/cRMMessaging/latest/actions/update-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "phone": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cRMMessaging/latest/actions/update-contact', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "phone": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `phone` | string | yes | Contact phone number. |
| `firstName` | string | no |  |
| `lastName` | string | no |  |
| `email` | string | no |  |
| `groupName` | string | no |  |
| `custom1` | string | no |  |
| `custom2` | string | no |  |
| `custom3` | string | no |  |
| `custom4` | string | no |  |
| `custom5` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `status` | number |  |

## Native endpoint

Through the native CRM Messaging API, this operation is `POST /index.php/Api/updateContact` (base URL `https://app.crm-messaging.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-contact.md) for the provider-specific parameters and requirements.

