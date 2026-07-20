# Farmbrite: Update contact

Updates an existing contact in Farmbrite.

```
PUT https://connect.mindcloud.co/v1/universal/farmbrite/latest/actions/update-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Farmbrite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/farmbrite/latest/actions/update-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contactId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/farmbrite/latest/actions/update-contact', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contactId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contactId` | string | yes |  |
| `phone` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cell": "string",
      "company": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "doNotMail": true,
      "email": "ava@example.com",
      "fax": "string",
      "firstName": "Ava",
      "id": "string",
      "label": "string",
      "lastName": "Chen",
      "phone": "string",
      "taxExempt": true,
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cell` | string |  |
| `company` | string |  |
| `createdAt` | date |  |
| `description` | string |  |
| `doNotMail` | boolean |  |
| `email` | string |  |
| `fax` | string |  |
| `firstName` | string |  |
| `id` | string |  |
| `label` | string |  |
| `lastName` | string |  |
| `phone` | string |  |
| `taxExempt` | boolean |  |
| `type` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Farmbrite API, this operation is `PUT /contacts/:contact_id` (base URL `https://api.farmbrite.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-contact.md) for the provider-specific parameters and requirements.

