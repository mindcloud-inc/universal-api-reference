# Moskit: Update Company

Updates an existing company in Moskit.

```
PUT https://connect.mindcloud.co/v1/universal/moskit/latest/actions/update-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Moskit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/moskit/latest/actions/update-company" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "createdBy.id": "154348",
  "id": "14310499",
  "name": "TV Globo",
  "responsible.id": "154348"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/moskit/latest/actions/update-company', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "createdBy.id": "154348",
    "id": "14310499",
    "name": "TV Globo",
    "responsible.id": "154348"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `cnpj` | string | no | Optional CNPJ for the company. |
| `createdBy.id` | number | yes | Moskit user ID that owns the creation record. Example: `154348`. |
| `domain` | string | no | Optional company domain. |
| `id` | number | yes | Moskit company ID. Example: `14310499`. |
| `name` | string | yes | Company name. Example: `TV Globo`. |
| `responsible.id` | number | yes | Moskit user ID responsible for the company. Example: `154348`. |

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
      "createdBy": {
        "id": 1
      },
      "dateCreated": "2026-05-07T12:00:00.000Z",
      "deals": [
        [
          {}
        ]
      ],
      "emails": [
        [
          {}
        ]
      ],
      "employees": [
        [
          {}
        ]
      ],
      "entityCustomFields": [
        [
          {}
        ]
      ],
      "id": 1,
      "name": "Ava Chen",
      "notes": "string",
      "origin": "string",
      "phones": [
        [
          {}
        ]
      ],
      "picture": "string",
      "primaryEmail": {
        "id": 1
      },
      "primaryPhone": {
        "id": 1
      },
      "responsible": {
        "id": 1
      },
      "source": "string"
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
| `createdBy` | object |  |
| `createdBy.id` | number |  |
| `dateCreated` | date |  |
| `deals[]` | array<object> |  |
| `deals[].id` | number |  |
| `emails[]` | array<object> |  |
| `emails[].address` | string |  |
| `emails[].id` | number |  |
| `employees[]` | array<object> |  |
| `employees[].contact` | object |  |
| `employees[].contact.id` | number |  |
| `entityCustomFields[]` | array<object> |  |
| `id` | number |  |
| `name` | string |  |
| `notes` | string |  |
| `origin` | string |  |
| `phones[]` | array<object> |  |
| `phones[].id` | number |  |
| `phones[].number` | string |  |
| `phones[].type` | object |  |
| `phones[].type.id` | number |  |
| `picture` | string |  |
| `primaryEmail` | object |  |
| `primaryEmail.id` | number |  |
| `primaryPhone` | object |  |
| `primaryPhone.id` | number |  |
| `responsible` | object |  |
| `responsible.id` | number |  |
| `source` | string |  |

## Native endpoint

Through the native Moskit API, this operation is `PUT companies/:id` (base URL `https://api.ms.prod.moskit.services/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-company.md) for the provider-specific parameters and requirements.

