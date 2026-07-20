# Harvest: Update Contact

Updates an existing contact in Harvest.

```
PUT https://connect.mindcloud.co/v1/universal/harvest/latest/actions/update-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Harvest `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/harvest/latest/actions/update-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/harvest/latest/actions/update-contact', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `clientId` | number | no |  |
| `id` | number | yes |  |
| `title` | string | no |  |
| `firstName` | string | no |  |
| `lastName` | string | no |  |
| `email` | string | no |  |
| `phoneOffice` | string | no |  |
| `phoneMobile` | string | no |  |
| `fax` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "client": {},
      "createdAt": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "fax": "string",
      "firstName": "Ava",
      "id": 1,
      "lastName": "Chen",
      "phoneMobile": "string",
      "phoneOffice": "string",
      "title": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `client` | object |  |
| `createdAt` | date |  |
| `email` | string |  |
| `fax` | string |  |
| `firstName` | string |  |
| `id` | number |  |
| `lastName` | string |  |
| `phoneMobile` | string |  |
| `phoneOffice` | string |  |
| `title` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Harvest API, this operation is `PATCH /v2/contacts/:id` (base URL `https://api.harvestapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-contact.md) for the provider-specific parameters and requirements.

