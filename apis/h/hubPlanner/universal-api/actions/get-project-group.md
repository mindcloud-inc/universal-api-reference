# Hub Planner: Get Project Group

Retrieves a project group from Hub Planner.

```
GET https://connect.mindcloud.co/v1/universal/hubPlanner/latest/actions/get-project-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hub Planner `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hubPlanner/latest/actions/get-project-group?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hubPlanner/latest/actions/get-project-group?${params}`, {
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
| `id` | string | yes | Hub Planner project group ID from the _id field. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_id": "string",
      "createdDate": "2026-05-07T12:00:00.000Z",
      "groupType": "string",
      "metadata": "string",
      "name": "Ava Chen",
      "optional": true,
      "parentGroupId": "string",
      "projects": [
        "string"
      ],
      "resources": [
        "string"
      ],
      "updatedDate": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_id` | string |  |
| `createdDate` | date |  |
| `groupType` | string |  |
| `metadata` | string |  |
| `name` | string |  |
| `optional` | boolean |  |
| `parentGroupId` | string |  |
| `projects` | array<string> |  |
| `resources` | array<string> |  |
| `updatedDate` | date |  |

## Native endpoint

Through the native Hub Planner API, this operation is `GET /projectgroup/:id` (base URL `https://api.hubplanner.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project-group.md) for the provider-specific parameters and requirements.

