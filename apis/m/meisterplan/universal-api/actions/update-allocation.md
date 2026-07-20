# Meisterplan: Update Allocation

Updates an existing project allocation in Meisterplan.

```
PUT https://connect.mindcloud.co/v1/universal/meisterplan/latest/actions/update-allocation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Meisterplan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/meisterplan/latest/actions/update-allocation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "scenarioId": "string",
  "projectId": "string",
  "allocationId": "string",
  "segments[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/meisterplan/latest/actions/update-allocation', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "scenarioId": "string",
    "projectId": "string",
    "allocationId": "string",
    "segments[]": [{}]
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
| `allocationId` | string | yes | Internal Meisterplan allocation identifier. |
| `segments[]` | array<object> | yes | Updated array of allocation segments. |

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

Through the native Meisterplan API, this operation is `PATCH /scenarios/:scenarioId/projects/:projectId/allocations/:allocationId` (base URL `https://api.us.meisterplan.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-allocation.md) for the provider-specific parameters and requirements.

