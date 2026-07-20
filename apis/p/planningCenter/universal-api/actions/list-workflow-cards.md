# Planning Center: List Workflow Cards

Retrieves workflow cards for a person in Planning Center.

```
GET https://connect.mindcloud.co/v1/universal/planningCenter/latest/actions/list-workflow-cards
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Planning Center `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/planningCenter/latest/actions/list-workflow-cards?connectionId=$CONNECTION_ID&limit=25&offset=0&personId=12345" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "personId": "12345"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/planningCenter/latest/actions/list-workflow-cards?${params}`, {
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
| `personId` | number | yes | Person ID Example: `12345`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `include` | string | no | Include associated resources Example: `assignee,current_step,workflow`. |
| `order` | string | no | Sort returned workflow cards Example: `-updated_at`. |
| `where` | object | no | Equality filters for workflow card fields |
| `where.assigneeId` | number | no | Query on a related assignee Example: `12345`. |
| `where.overdue` | boolean | no | Query on a specific overdue value Example: `true`. |
| `where.stage` | string | no | Query on a specific stage |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "calculatedDueAtInDaysAgo": 1,
        "completedAt": "2026-05-07T12:00:00.000Z",
        "createdAt": "2026-05-07T12:00:00.000Z",
        "flaggedForNotificationAt": "2026-05-07T12:00:00.000Z",
        "movedToStepAt": "2026-05-07T12:00:00.000Z",
        "overdue": true,
        "removedAt": "2026-05-07T12:00:00.000Z",
        "snoozeUntil": "2026-05-07T12:00:00.000Z",
        "stage": "string",
        "stickyAssignment": true,
        "updatedAt": "2026-05-07T12:00:00.000Z"
      },
      "id": "string",
      "relationships": {
        "assignee": {
          "data": {
            "id": "string",
            "type": "string"
          }
        },
        "currentStep": {
          "data": {
            "id": "string",
            "type": "string"
          }
        },
        "person": {
          "data": {
            "id": "string",
            "type": "string"
          }
        },
        "workflow": {
          "data": {
            "id": "string",
            "type": "string"
          }
        }
      },
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes.calculatedDueAtInDaysAgo` | number |  |
| `attributes.completedAt` | date |  |
| `attributes.createdAt` | date |  |
| `attributes.flaggedForNotificationAt` | date |  |
| `attributes.movedToStepAt` | date |  |
| `attributes.overdue` | boolean |  |
| `attributes.removedAt` | date |  |
| `attributes.snoozeUntil` | date |  |
| `attributes.stage` | string |  |
| `attributes.stickyAssignment` | boolean |  |
| `attributes.updatedAt` | date |  |
| `id` | string |  |
| `relationships.assignee.data.id` | string |  |
| `relationships.assignee.data.type` | string |  |
| `relationships.currentStep.data.id` | string |  |
| `relationships.currentStep.data.type` | string |  |
| `relationships.person.data.id` | string |  |
| `relationships.person.data.type` | string |  |
| `relationships.workflow.data.id` | string |  |
| `relationships.workflow.data.type` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Planning Center API, this operation is `GET /people/v2/people/:person_id/workflow_cards` (base URL `https://api.planningcenteronline.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-workflow-cards.md) for the provider-specific parameters and requirements.

