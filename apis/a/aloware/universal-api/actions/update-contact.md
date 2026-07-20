# Aloware: Update Contact

Updates an existing contact in Aloware.

```
PUT https://connect.mindcloud.co/v1/universal/aloware/latest/actions/update-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Aloware `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/aloware/latest/actions/update-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "phoneNumber": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/aloware/latest/actions/update-contact', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "phoneNumber": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `companyName` | string | no | Updated company name. |
| `email` | string | no | Updated contact email address. |
| `name` | string | no | Updated full contact name. |
| `notes` | string | no | Updated notes to save on the contact. |
| `phoneNumber` | string | yes | Primary phone number for the contact to update. |
| `ringGroupId` | string | no | Assign the contact through a ring group. |
| `userId` | string | no | Assign the contact to a specific user. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contactId": 1,
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contactId` | number |  |
| `message` | string |  |

## Native endpoint

Through the native Aloware API, this operation is `POST /api/v1/webhook/forms` (base URL `https://app.aloware.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-contact.md) for the provider-specific parameters and requirements.

