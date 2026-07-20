# Moxie: Create Client

Creates a new client in Moxie.

```
POST https://connect.mindcloud.co/v1/universal/moxie/latest/actions/create-client
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Moxie `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/moxie/latest/actions/create-client" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "clientType": "string",
  "currency": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/moxie/latest/actions/create-client', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "clientType": "string",
    "currency": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Business name for the client. |
| `clientType` | string | yes | Either Client or Prospect. |
| `currency` | string | yes | ISO 4217 currency code for the client. |
| `website` | string | no | Website URL for the client. |
| `phone` | string | no | Primary phone number for the client. |
| `notes` | string | no | Internal notes for the client. |
| `paymentTerms` | object | no | Payment terms object for the client. |
| `contacts` | list<object> | no | Optional list of contacts to create with the client. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": 1,
      "clientType": "string",
      "contacts": [
        {}
      ],
      "id": "string",
      "name": "Ava Chen",
      "paymentTerms": {},
      "phone": "string",
      "sampleData": true,
      "website": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | number |  |
| `clientType` | string |  |
| `contacts` | array<object> |  |
| `id` | string |  |
| `name` | string |  |
| `paymentTerms` | object |  |
| `phone` | string |  |
| `sampleData` | boolean |  |
| `website` | string |  |

## Native endpoint

Through the native Moxie API, this operation is `POST /action/clients/create` (base URL `https://pod01.withmoxie.com/api/public`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-client.md) for the provider-specific parameters and requirements.

