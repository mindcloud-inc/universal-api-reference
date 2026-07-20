# Karma CRM: Create Contact

Creates a new contact in Karma CRM.

```
POST https://connect.mindcloud.co/v1/universal/karmaCRM/latest/actions/create-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Karma CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/karmaCRM/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contact": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/karmaCRM/latest/actions/create-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contact": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contact` | object | yes | Contact payload object exactly as documented by Karma CRM. Pass the nested contact fields inside this object. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "background": "string",
      "contactStageId": {},
      "contactStatusId": {},
      "createdAt": "string",
      "createdById": 1,
      "department": {},
      "firstName": "Ava",
      "id": 1,
      "industryId": {},
      "lastName": "Chen",
      "organizationId": 1,
      "position": "string",
      "private": true,
      "privateNotes": {},
      "referralSourceId": {},
      "updatedAt": "string",
      "userId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `background` | string |  |
| `contactStageId` | object |  |
| `contactStatusId` | object |  |
| `createdAt` | string |  |
| `createdById` | number |  |
| `department` | object |  |
| `firstName` | string |  |
| `id` | number |  |
| `industryId` | object |  |
| `lastName` | string |  |
| `organizationId` | number |  |
| `position` | string |  |
| `private` | boolean |  |
| `privateNotes` | object |  |
| `referralSourceId` | object |  |
| `updatedAt` | string |  |
| `userId` | number |  |

## Native endpoint

Through the native Karma CRM API, this operation is `POST /api/v3/contacts.json` (base URL `https://app.karmacrm.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contact.md) for the provider-specific parameters and requirements.

