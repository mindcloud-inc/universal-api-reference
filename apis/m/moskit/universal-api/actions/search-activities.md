# Moskit: Search Activities

Finds activities in Moskit by search criteria.

```
GET https://connect.mindcloud.co/v1/universal/moskit/latest/actions/search-activities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Moskit `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moskit/latest/actions/search-activities?connectionId=$CONNECTION_ID&limit=25&offset=0&conditions%5B%5D=%5Bobject%20Object%5D&conditions%5B%5D.expression=like&conditions%5B%5D.field=title" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "conditions[]": "[object Object]",
  "conditions[].expression": "like",
  "conditions[].field": "title"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moskit/latest/actions/search-activities?${params}`, {
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
| `conditions[].field` | string | yes | Search field key returned by GET /activities/search. Example: `title`. |
| `conditions[].values[]` | array<string> | no | Optional values array for the condition. Leave empty for null or not_null expressions. Example: `Ligação`. |

## Response

```json
{
  "success": true,
  "data": [
    {
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
      "deals": [
        [
          {}
        ]
      ],
      "doneDate": "2026-05-07T12:00:00.000Z",
      "doneNotes": "string",
      "doneSource": "string",
      "doneUser": {
        "id": 1
      },
      "dueDate": "2026-05-07T12:00:00.000Z",
      "duration": 1,
      "entityCustomFields": [
        [
          {}
        ]
      ],
      "firstTry": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "lastTry": "2026-05-07T12:00:00.000Z",
      "notes": "string",
      "origin": "string",
      "projects": [
        [
          {}
        ]
      ],
      "responsible": {
        "id": 1
      },
      "source": "string",
      "title": "string",
      "totalDays": 1,
      "totalTries": 1,
      "type": {
        "id": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `companies[]` | array<object> |  |
| `companies[].id` | number |  |
| `contacts[]` | array<object> |  |
| `contacts[].id` | number |  |
| `createdBy` | object |  |
| `createdBy.id` | number |  |
| `dateCreated` | date |  |
| `deals[]` | array<object> |  |
| `deals[].id` | number |  |
| `doneDate` | date |  |
| `doneNotes` | string |  |
| `doneSource` | string |  |
| `doneUser` | object |  |
| `doneUser.id` | number |  |
| `dueDate` | date |  |
| `duration` | number |  |
| `entityCustomFields[]` | array<object> |  |
| `firstTry` | date |  |
| `id` | number |  |
| `lastTry` | date |  |
| `notes` | string |  |
| `origin` | string |  |
| `projects[]` | array<object> |  |
| `projects[].id` | number |  |
| `responsible` | object |  |
| `responsible.id` | number |  |
| `source` | string |  |
| `title` | string |  |
| `totalDays` | number |  |
| `totalTries` | number |  |
| `type` | object |  |
| `type.id` | number |  |

## Native endpoint

Through the native Moskit API, this operation is `POST activities/search` (base URL `https://api.ms.prod.moskit.services/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-activities.md) for the provider-specific parameters and requirements.

