# MoneyBird: Update Contact

Updates an existing contact in MoneyBird.

```
PUT https://connect.mindcloud.co/v1/universal/moneyBird/latest/actions/update-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MoneyBird `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/moneyBird/latest/actions/update-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "administrationId": "string",
  "contactId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/moneyBird/latest/actions/update-contact', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "administrationId": "string",
    "contactId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `administrationId` | string | yes | Moneybird administration ID. |
| `contactId` | string | yes | Moneybird contact ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "administrationId": "string",
      "archived": true,
      "city": "string",
      "companyName": "Ava Chen",
      "country": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "customerId": "string",
      "email": "ava@example.com",
      "firstname": "Ava",
      "id": "string",
      "lastname": "Chen",
      "phone": "string",
      "taxNumber": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "version": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `administrationId` | string |  |
| `archived` | boolean |  |
| `city` | string |  |
| `companyName` | string |  |
| `country` | string |  |
| `createdAt` | date |  |
| `customerId` | string |  |
| `email` | string |  |
| `firstname` | string |  |
| `id` | string |  |
| `lastname` | string |  |
| `phone` | string |  |
| `taxNumber` | string |  |
| `updatedAt` | date |  |
| `version` | number |  |

## Native endpoint

Through the native MoneyBird API, this operation is `PATCH /:administrationId/contacts/:contactId.json` (base URL `https://moneybird.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-contact.md) for the provider-specific parameters and requirements.

