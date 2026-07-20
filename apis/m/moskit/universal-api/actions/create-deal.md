# Moskit: Create Deal

Creates a new deal in Moskit.

```
POST https://connect.mindcloud.co/v1/universal/moskit/latest/actions/create-deal
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Moskit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/moskit/latest/actions/create-deal" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "createdBy.id": 1,
  "responsible.id": 1,
  "status": "string",
  "stage.id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/moskit/latest/actions/create-deal', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "createdBy.id": 1,
    "responsible.id": 1,
    "status": "string",
    "stage.id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes |  |
| `createdBy.id` | number | yes |  |
| `responsible.id` | number | yes |  |
| `status` | string | yes |  |
| `stage.id` | number | yes |  |
| `previsionCloseDate` | date | no |  |
| `price` | number | no |  |
| `closeDate` | date | no |  |
| `lostReason.id` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "activities": [
        [
          {}
        ]
      ],
      "closeDate": "2026-05-07T12:00:00.000Z",
      "companies": [
        [
          {}
        ]
      ],
      "contacts": [
        [
          {}
        ]
      ],
      "createdBy": {
        "id": 1
      },
      "dateCreated": "2026-05-07T12:00:00.000Z",
      "entityCustomFields": [
        [
          {}
        ]
      ],
      "id": 1,
      "lostReason": {
        "id": 1
      },
      "name": "Ava Chen",
      "origin": "string",
      "previsionCloseDate": "2026-05-07T12:00:00.000Z",
      "price": 1,
      "responsible": {
        "id": 1
      },
      "source": "string",
      "stage": {
        "id": 1
      },
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activities[]` | array<object> |  |
| `activities[].id` | number |  |
| `closeDate` | date |  |
| `companies[]` | array<object> |  |
| `companies[].id` | number |  |
| `contacts[]` | array<object> |  |
| `contacts[].id` | number |  |
| `createdBy` | object |  |
| `createdBy.id` | number |  |
| `dateCreated` | date |  |
| `entityCustomFields[]` | array<object> |  |
| `id` | number |  |
| `lostReason` | object |  |
| `lostReason.id` | number |  |
| `name` | string |  |
| `origin` | string |  |
| `previsionCloseDate` | date |  |
| `price` | number |  |
| `responsible` | object |  |
| `responsible.id` | number |  |
| `source` | string |  |
| `stage` | object |  |
| `stage.id` | number |  |
| `status` | string |  |

## Native endpoint

Through the native Moskit API, this operation is `POST deals` (base URL `https://api.ms.prod.moskit.services/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-deal.md) for the provider-specific parameters and requirements.

