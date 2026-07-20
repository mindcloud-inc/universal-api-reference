# Timizer: Update Contracted Company

Updates an existing contracted company in Timizer.

```
PUT https://connect.mindcloud.co/v1/universal/timizer/latest/actions/update-contracted-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timizer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/timizer/latest/actions/update-contracted-company" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/timizer/latest/actions/update-contracted-company', {
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
| `archived` | boolean | no | Whether the contracted company is archived. |
| `city` | string | no | Updated city of the contracted company. |
| `fullAddress` | string | no | Updated full address of the contracted company. |
| `id` | number | yes | ID of the contracted company. |
| `name` | string | no | Updated name of the contracted company. |
| `postalCode` | string | no | Updated postal code of the contracted company. |
| `uniqueIdentifier` | string | no | Updated unique identifier of the contracted company. |

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

Through the native Timizer API, this operation is `PATCH /app/contracted/:id` (base URL `https://api.timizer.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-contracted-company.md) for the provider-specific parameters and requirements.

