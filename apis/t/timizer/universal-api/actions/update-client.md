# Timizer: Update Client

Updates an existing client in Timizer.

```
PUT https://connect.mindcloud.co/v1/universal/timizer/latest/actions/update-client
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timizer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/timizer/latest/actions/update-client" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/timizer/latest/actions/update-client', {
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
| `archived` | boolean | no | Whether the client is archived. |
| `city` | string | no | Updated city of the client. |
| `country` | string | no | Updated country code alpha-2 of the client. |
| `fullAddress` | string | no | Updated full address of the client. |
| `id` | number | yes | ID of the client. |
| `name` | string | no | Updated name of the client. |
| `postalCode` | string | no | Updated postal code of the client. |
| `uniqueIdentifier` | string | no | Updated unique identifier of the client. |

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

Through the native Timizer API, this operation is `PATCH /app/clients/:id` (base URL `https://api.timizer.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-client.md) for the provider-specific parameters and requirements.

