# Planning Center: List Workflows

Retrieves workflows from Planning Center.

```
GET https://connect.mindcloud.co/v1/universal/planningCenter/latest/actions/list-workflows
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Planning Center `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/planningCenter/latest/actions/list-workflows?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/planningCenter/latest/actions/list-workflows?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `include` | string | no | Include associated resources Example: `category,steps`. |
| `order` | string | no | Sort returned workflows Example: `-updated_at`. |
| `where` | object | no | Equality filters for workflow fields |
| `where.archivedAt` | date | no | Query on a specific archived_at Example: `2000-01-01T12:00:00Z`. |
| `where.campusId` | number | no | Query on a specific campus_id Example: `12345`. |
| `where.createdAt` | date | no | Query on a specific created_at Example: `2000-01-01T12:00:00Z`. |
| `where.deletedAt` | date | no | Query on a specific deleted_at Example: `2000-01-01T12:00:00Z`. |
| `where.id` | number | no | Query on a specific id Example: `12345`. |
| `where.name` | string | no | Query on a specific name Example: `Follow Up`. |
| `where.updatedAt` | date | no | Query on a specific updated_at Example: `2000-01-01T12:00:00Z`. |
| `where.workflowCategoryId` | number | no | Query on a specific workflow_category_id Example: `12345`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "archivedAt": "2026-05-07T12:00:00.000Z",
        "campusId": "string",
        "completedCardCount": 1,
        "createdAt": "2026-05-07T12:00:00.000Z",
        "deletedAt": "2026-05-07T12:00:00.000Z",
        "myDueSoonCardCount": 1,
        "myOverdueCardCount": 1,
        "myReadyCardCount": 1,
        "name": "Ava Chen",
        "recentlyViewed": true,
        "totalCardsCount": 1,
        "totalOverdueCardCount": 1,
        "totalReadyAndSnoozedCardCount": 1,
        "totalReadyCardCount": 1,
        "totalStepsCount": 1,
        "totalUnassignedCardCount": 1,
        "totalUnassignedStepsCount": 1,
        "updatedAt": "2026-05-07T12:00:00.000Z",
        "workflowCategoryId": "string"
      },
      "id": "string",
      "relationships": {
        "campus": {
          "data": {
            "id": "string",
            "type": "string"
          }
        },
        "workflowCategory": {
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
| `attributes.archivedAt` | date |  |
| `attributes.campusId` | string |  |
| `attributes.completedCardCount` | number |  |
| `attributes.createdAt` | date |  |
| `attributes.deletedAt` | date |  |
| `attributes.myDueSoonCardCount` | number |  |
| `attributes.myOverdueCardCount` | number |  |
| `attributes.myReadyCardCount` | number |  |
| `attributes.name` | string |  |
| `attributes.recentlyViewed` | boolean |  |
| `attributes.totalCardsCount` | number |  |
| `attributes.totalOverdueCardCount` | number |  |
| `attributes.totalReadyAndSnoozedCardCount` | number |  |
| `attributes.totalReadyCardCount` | number |  |
| `attributes.totalStepsCount` | number |  |
| `attributes.totalUnassignedCardCount` | number |  |
| `attributes.totalUnassignedStepsCount` | number |  |
| `attributes.updatedAt` | date |  |
| `attributes.workflowCategoryId` | string |  |
| `id` | string |  |
| `relationships.campus.data.id` | string |  |
| `relationships.campus.data.type` | string |  |
| `relationships.workflowCategory.data.id` | string |  |
| `relationships.workflowCategory.data.type` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Planning Center API, this operation is `GET /people/v2/workflows` (base URL `https://api.planningcenteronline.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-workflows.md) for the provider-specific parameters and requirements.

