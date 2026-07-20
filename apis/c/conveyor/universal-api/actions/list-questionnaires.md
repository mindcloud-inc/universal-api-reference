# Conveyor: List Questionnaires

Retrieves questionnaires from Conveyor with optional filters.

```
GET https://connect.mindcloud.co/v1/universal/conveyor/latest/actions/list-questionnaires
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Conveyor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/conveyor/latest/actions/list-questionnaires?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/conveyor/latest/actions/list-questionnaires?${params}`, {
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
| `status` | string | no | Questionnaire status filter. |
| `productLineIds` | string<string> | no | Product line identifiers to filter questionnaires. |
| `createdAtStart` | date | no | Start of created-at date range. |
| `createdAtEnd` | date | no | End of created-at date range. |
| `completedAtStart` | date | no | Start of completed-at date range. |
| `completedAtEnd` | date | no | End of completed-at date range. |
| `dueAtStart` | date | no | Start of due-at date range. |
| `dueAtEnd` | date | no | End of due-at date range. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_embedded": {
        "questionnaires": [
          {
            "domain": "string",
            "due_at": "2026-05-07T12:00:00.000Z",
            "id": "string",
            "status": "string"
          }
        ]
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_embedded` | object |  |
| `_embedded.questionnaires` | array<object> |  |
| `_embedded.questionnaires[].domain` | string |  |
| `_embedded.questionnaires[].due_at` | date |  |
| `_embedded.questionnaires[].id` | string |  |
| `_embedded.questionnaires[].status` | string |  |

## Native endpoint

Through the native Conveyor API, this operation is `GET /v2/questionnaires` (base URL `https://api.conveyor.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-questionnaires.md) for the provider-specific parameters and requirements.

