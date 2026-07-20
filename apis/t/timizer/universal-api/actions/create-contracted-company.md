# Timizer: Create Contracted Company

Creates a contracted company in Timizer.

```
POST https://connect.mindcloud.co/v1/universal/timizer/latest/actions/create-contracted-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timizer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/timizer/latest/actions/create-contracted-company" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/timizer/latest/actions/create-contracted-company', {
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
| `city` | string | no | City of the contracted company. |
| `fullAddress` | string | no | Full address of the contracted company. |
| `name` | string | yes | Name of the contracted company. |
| `postalCode` | string | no | Postal code of the contracted company. |
| `teamId` | number | no | Team ID to make the contracted company available to the team. |
| `uniqueIdentifier` | string | no | Unique identifier of the contracted company. |

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

Through the native Timizer API, this operation is `POST /app/contracted` (base URL `https://api.timizer.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contracted-company.md) for the provider-specific parameters and requirements.

