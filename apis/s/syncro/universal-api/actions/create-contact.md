# Syncro: Create Contact

Creates a new contact in Syncro.

```
POST https://connect.mindcloud.co/v1/universal/syncro/latest/actions/create-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Syncro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/syncro/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customerId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/syncro/latest/actions/create-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customerId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customerId` | number | yes |  |
| `name` | string | no |  |
| `address1` | string | no |  |
| `address2` | string | no |  |
| `city` | string | no |  |
| `state` | string | no |  |
| `zip` | string | no |  |
| `email` | string | no |  |
| `phone` | string | no |  |
| `mobile` | string | no |  |
| `notes` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": 1,
      "address1": "string",
      "city": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "customerId": 1,
      "email": "ava@example.com",
      "id": 1,
      "name": "Ava Chen",
      "notes": "string",
      "optOut": true,
      "phone": "string",
      "processedPhone": "string",
      "sinceUpdatedAt": "2026-05-07T12:00:00.000Z",
      "state": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | number |  |
| `address1` | string |  |
| `city` | string |  |
| `createdAt` | date |  |
| `customerId` | number |  |
| `email` | string |  |
| `id` | number |  |
| `name` | string |  |
| `notes` | string |  |
| `optOut` | boolean |  |
| `phone` | string |  |
| `processedPhone` | string |  |
| `sinceUpdatedAt` | date |  |
| `state` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Syncro API, this operation is `POST /contacts` (base URL `https://mindcloud.syncromsp.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contact.md) for the provider-specific parameters and requirements.

