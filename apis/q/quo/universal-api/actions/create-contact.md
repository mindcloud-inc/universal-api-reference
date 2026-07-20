# Quo: Create Contact

Creates a new contact in Quo.

```
POST https://connect.mindcloud.co/v1/universal/quo/latest/actions/create-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Quo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/quo/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/quo/latest/actions/create-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `createdByUserId` | string | no |  |
| `customFields[]` | array<object> | no |  |
| `defaultFields` | object | no |  |
| `defaultFields.company` | string | no |  |
| `defaultFields.emails[]` | array<string> | no |  |
| `defaultFields.firstName` | string | no |  |
| `defaultFields.lastName` | string | no |  |
| `defaultFields.phoneNumbers[]` | array<string> | no |  |
| `defaultFields.role` | string | no |  |
| `externalId` | string | no |  |
| `source` | string | no |  |
| `sourceUrl` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "createdByUserId": "string",
      "defaultFields": {
        "company": {},
        "firstName": "Ava",
        "lastName": "Chen",
        "role": {}
      },
      "externalId": {},
      "id": "string",
      "source": "string",
      "sourceUrl": {},
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `createdByUserId` | string |  |
| `defaultFields.company` | object |  |
| `defaultFields.firstName` | string |  |
| `defaultFields.lastName` | string |  |
| `defaultFields.role` | object |  |
| `externalId` | object |  |
| `id` | string |  |
| `source` | string |  |
| `sourceUrl` | object |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Quo API, this operation is `POST /contacts` (base URL `https://api.openphone.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contact.md) for the provider-specific parameters and requirements.

