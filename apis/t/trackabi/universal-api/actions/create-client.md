# Trackabi: Create Client

Creates a new client in Trackabi.

```
POST https://connect.mindcloud.co/v1/universal/trackabi/latest/actions/create-client
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Trackabi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/trackabi/latest/actions/create-client" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/trackabi/latest/actions/create-client', {
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
| `name` | string | no | The client's name. |
| `shortName` | string | no | Short name of the client. |
| `contactPerson` | string | no | Contact person. |
| `address` | string | no | Address of the client. |
| `email` | string | no | Client's email. |
| `phone` | string | no | Client's phone number. |
| `notes` | string | no | Additional notes about the client. |
| `currency` | string | no | Client's currency. |
| `hourlyRate` | number | no | Hourly rate. |
| `costHourlyRate` | number | no | Cost hourly rate. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": "string",
      "contactPerson": "string",
      "costHourlyRate": 1,
      "currency": "string",
      "email": "ava@example.com",
      "hourlyRate": 1,
      "id": 1,
      "logo": "string",
      "name": "Ava Chen",
      "notes": "string",
      "phone": "string",
      "shortName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string |  |
| `contactPerson` | string |  |
| `costHourlyRate` | number |  |
| `currency` | string |  |
| `email` | string |  |
| `hourlyRate` | number |  |
| `id` | number |  |
| `logo` | string |  |
| `name` | string |  |
| `notes` | string |  |
| `phone` | string |  |
| `shortName` | string |  |

## Native endpoint

Through the native Trackabi API, this operation is `POST /api/v1/clients` (base URL `https://api.trackabi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-client.md) for the provider-specific parameters and requirements.

