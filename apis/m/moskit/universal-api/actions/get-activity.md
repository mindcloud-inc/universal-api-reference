# Moskit: Get Activity

Retrieves an activity from Moskit.

```
GET https://connect.mindcloud.co/v1/universal/moskit/latest/actions/get-activity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Moskit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moskit/latest/actions/get-activity?connectionId=$CONNECTION_ID&id=74883431" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "74883431"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moskit/latest/actions/get-activity?${params}`, {
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
| `id` | number | yes | Moskit activity ID. Example: `74883431`. |

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

Through the native Moskit API, this operation is `GET activities/:id` (base URL `https://api.ms.prod.moskit.services/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-activity.md) for the provider-specific parameters and requirements.

