# Clientary: Get Client

Retrieves a client from Clientary by client ID.

```
GET https://connect.mindcloud.co/v1/universal/clientary/latest/actions/get-client
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clientary `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clientary/latest/actions/get-client?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clientary/latest/actions/get-client?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The Clientary client ID. |

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

Through the native Clientary API, this operation is `GET /clients/:id` (base URL `https://{{credentials.subdomain}}.clientary.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-client.md) for the provider-specific parameters and requirements.

