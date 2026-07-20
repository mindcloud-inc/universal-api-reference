# Sozuri (Kenya) SMS: Update Contact

Updates an existing contact in Sozuri.

```
PUT https://connect.mindcloud.co/v1/universal/sozuriKenyaSMS/latest/actions/update-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sozuri (Kenya) SMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/sozuriKenyaSMS/latest/actions/update-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contactIdOrMobile": "string",
  "contact": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sozuriKenyaSMS/latest/actions/update-contact', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contactIdOrMobile": "string",
    "contact": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contactIdOrMobile` | string | yes | The contact ID or mobile number to update. |
| `group` | string | no | The group name to associate with the updated contact. |
| `contact` | object | yes | The contact fields to update. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |

## Native endpoint

Through the native Sozuri (Kenya) SMS API, this operation is `PUT /contacts/:contactIdOrMobile` (base URL `https://sozuri.net/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-contact.md) for the provider-specific parameters and requirements.

