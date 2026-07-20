# Karma CRM: Create Company

Creates a new company in Karma CRM.

```
POST https://connect.mindcloud.co/v1/universal/karmaCRM/latest/actions/create-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Karma CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/karmaCRM/latest/actions/create-company" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "company": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/karmaCRM/latest/actions/create-company', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "company": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `company` | object | yes | Company payload object exactly as documented by Karma CRM. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "avatarFileName": {},
      "background": "string",
      "createdAt": "string",
      "createdById": 1,
      "id": 1,
      "industryId": {},
      "name": "Ava Chen",
      "organizationId": 1,
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
| `avatarFileName` | object |  |
| `background` | string |  |
| `createdAt` | string |  |
| `createdById` | number |  |
| `id` | number |  |
| `industryId` | object |  |
| `name` | string |  |
| `organizationId` | number |  |
| `private` | boolean |  |
| `privateNotes` | object |  |
| `referralSourceId` | object |  |
| `updatedAt` | string |  |
| `userId` | number |  |

## Native endpoint

Through the native Karma CRM API, this operation is `POST /api/v3/companies.json` (base URL `https://app.karmacrm.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-company.md) for the provider-specific parameters and requirements.

