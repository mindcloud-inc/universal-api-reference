# Meisterplan: Create Or Update Allocation

Creates or updates project allocations in Meisterplan.

```
POST https://connect.mindcloud.co/v1/universal/meisterplan/latest/actions/create-or-update-allocation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Meisterplan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/meisterplan/latest/actions/create-or-update-allocation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "scenarioId": "string",
  "projectId": "string",
  "allocatedEntity": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/meisterplan/latest/actions/create-or-update-allocation', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "scenarioId": "string",
    "projectId": "string",
    "allocatedEntity": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `scenarioId` | string | yes | Internal Meisterplan scenario identifier. |
| `projectId` | string | yes | Internal Meisterplan project identifier. |
| `allocatedEntity` | object | yes | Allocated entity object with id, type, and optional projectRole. |
| `segments[]` | array<object> | no | Array of allocation segments. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "allocatedEntity": {
        "id": "string",
        "projectRole": "string",
        "type": "string"
      },
      "id": "string",
      "segments": [
        {
          "finish": "2026-05-07T12:00:00.000Z",
          "hours": 1,
          "start": "2026-05-07T12:00:00.000Z"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allocatedEntity.id` | string | Allocated entity ID |
| `allocatedEntity.projectRole` | string | Project role ID |
| `allocatedEntity.type` | string | Allocated entity type |
| `id` | string | Allocation ID |
| `segments[].finish` | date | Segment finish date |
| `segments[].hours` | number | Segment hours |
| `segments[].start` | date | Segment start date |

## Native endpoint

Through the native Meisterplan API, this operation is `POST /scenarios/:scenarioId/projects/:projectId/allocations` (base URL `https://api.us.meisterplan.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-or-update-allocation.md) for the provider-specific parameters and requirements.

