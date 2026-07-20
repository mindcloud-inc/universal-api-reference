# Timizer: Create Client

Creates a client in Timizer.

```
POST https://connect.mindcloud.co/v1/universal/timizer/latest/actions/create-client
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timizer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/timizer/latest/actions/create-client" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/timizer/latest/actions/create-client', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `city` | string | no | City of the client. |
| `country` | string | no | Country code alpha-2 of the client. |
| `fullAddress` | string | no | Full address of the client. |
| `name` | string | yes | Name of the client. |
| `postalCode` | string | no | Postal code of the client. |
| `teamId` | number | no | Team ID to make the client available to the team. |
| `uniqueIdentifier` | string | no | Unique identifier of the client. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "city": "string",
      "contacts": [
        {}
      ],
      "country": "string",
      "fullAddress": "string",
      "id": 1,
      "name": "Ava Chen",
      "note": "string",
      "pennylaneId": 1,
      "postalCode": "string",
      "siret": "string",
      "teamId": 1,
      "uniqueIdentifier": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean |  |
| `city` | string |  |
| `contacts` | array<object> |  |
| `country` | string |  |
| `fullAddress` | string |  |
| `id` | number |  |
| `name` | string |  |
| `note` | string |  |
| `pennylaneId` | number |  |
| `postalCode` | string |  |
| `siret` | string |  |
| `teamId` | number |  |
| `uniqueIdentifier` | string |  |

## Native endpoint

Through the native Timizer API, this operation is `POST /app/clients` (base URL `https://api.timizer.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-client.md) for the provider-specific parameters and requirements.

