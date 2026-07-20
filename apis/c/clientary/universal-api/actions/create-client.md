# Clientary: Create Client

Creates a new client in Clientary.

```
POST https://connect.mindcloud.co/v1/universal/clientary/latest/actions/create-client
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clientary `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/clientary/latest/actions/create-client" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "client.name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clientary/latest/actions/create-client', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "client.name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `client.name` | string | yes | The client name. |
| `client.number` | string | no | Optional unique client number. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "account": {
        "currencyCode": "string"
      },
      "address": "string",
      "amountOutstanding": 1,
      "city": "string",
      "contactViewable": true,
      "country": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": 1,
      "name": "Ava Chen",
      "notesCount": 1,
      "number": "string",
      "pendingInvoices": 1,
      "state": "string",
      "status": "string",
      "unbilledProjectsCount": 1,
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "usersCount": 1,
      "wasLead": true,
      "website": "string",
      "zip": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account.currencyCode` | string |  |
| `address` | string |  |
| `amountOutstanding` | number |  |
| `city` | string |  |
| `contactViewable` | boolean |  |
| `country` | string |  |
| `createdAt` | date |  |
| `description` | string |  |
| `id` | number |  |
| `name` | string |  |
| `notesCount` | number |  |
| `number` | string |  |
| `pendingInvoices` | number |  |
| `state` | string |  |
| `status` | string |  |
| `unbilledProjectsCount` | number |  |
| `updatedAt` | date |  |
| `usersCount` | number |  |
| `wasLead` | boolean |  |
| `website` | string |  |
| `zip` | string |  |

## Native endpoint

Through the native Clientary API, this operation is `POST /clients` (base URL `https://{{credentials.subdomain}}.clientary.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-client.md) for the provider-specific parameters and requirements.

