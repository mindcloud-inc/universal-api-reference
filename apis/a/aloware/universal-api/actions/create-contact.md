# Aloware: Create Contact

Creates a new contact in Aloware.

```
POST https://connect.mindcloud.co/v1/universal/aloware/latest/actions/create-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Aloware `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/aloware/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "phoneNumber": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/aloware/latest/actions/create-contact', {
  method: 'POST',
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
| `phoneNumber` | string | yes | Primary phone number for the contact. |
| `name` | string | no | Full contact name. |
| `email` | string | no | Contact email address. |
| `companyName` | string | no | Company name for the contact. |
| `userId` | string | no | Assign the contact to a specific user. |
| `ringGroupId` | string | no | Assign the contact through a ring group. |
| `notes` | string | no | Notes to save on the contact. |
| `sequenceId` | string | no | Optional sequence to enroll the contact into. |

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

Through the native Aloware API, this operation is `POST /api/v1/webhook/forms` (base URL `https://app.aloware.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contact.md) for the provider-specific parameters and requirements.

