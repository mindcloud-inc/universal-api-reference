# Farmbrite: Create contact

Creates a new contact in Farmbrite.

```
POST https://connect.mindcloud.co/v1/universal/farmbrite/latest/actions/create-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Farmbrite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/farmbrite/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "firstName": "Ava",
  "lastName": "Chen",
  "email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/farmbrite/latest/actions/create-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "firstName": "Ava",
    "lastName": "Chen",
    "email": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `firstName` | string | yes |  |
| `lastName` | string | yes |  |
| `email` | string | yes |  |

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

Through the native Farmbrite API, this operation is `POST /contacts` (base URL `https://api.farmbrite.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contact.md) for the provider-specific parameters and requirements.

