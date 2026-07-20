# Moskit: Search Companies

Finds companies in Moskit by search criteria.

```
GET https://connect.mindcloud.co/v1/universal/moskit/latest/actions/search-companies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Moskit `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moskit/latest/actions/search-companies?connectionId=$CONNECTION_ID&limit=25&offset=0&conditions%5B%5D=%5Bobject%20Object%5D&conditions%5B%5D.expression=like&conditions%5B%5D.field=name" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "conditions[]": "[object Object]",
  "conditions[].expression": "like",
  "conditions[].field": "name"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moskit/latest/actions/search-companies?${params}`, {
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
| `conditions[]` | array<object> | yes | Array of search conditions. Each item needs a field, expression, and optional values array. |
| `conditions[].expression` | string | yes | Search expression such as like, one_of, null, or not_null. Example: `like`. |
| `conditions[].field` | string | yes | Search field key returned by GET /companies/search. Example: `name`. |
| `conditions[].values[]` | array<string> | no | Optional values array for the condition. Leave empty for null or not_null expressions. Example: `TV Globo`. |

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

Through the native Moskit API, this operation is `POST companies/search` (base URL `https://api.ms.prod.moskit.services/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-companies.md) for the provider-specific parameters and requirements.

