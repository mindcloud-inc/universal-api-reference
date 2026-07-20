# Leiga: Create Sprint

Creates a new sprint in Leiga.

```
POST https://connect.mindcloud.co/v1/universal/leiga/latest/actions/create-sprint
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Leiga `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/leiga/latest/actions/create-sprint" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "projectId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/leiga/latest/actions/create-sprint', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "projectId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Sprint Name |
| `projectId` | number | yes | Project ID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assignee": 1,
      "assigneeName": "Ava Chen",
      "completeDate": 1,
      "endDate": 1,
      "goal": "string",
      "id": 1,
      "name": "Ava Chen",
      "projectId": "string",
      "startDate": 1,
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assignee` | number | Sprint owner ID. |
| `assigneeName` | string | Sprint owner name. |
| `completeDate` | number | Completion timestamp. |
| `endDate` | number | End timestamp. |
| `goal` | string | Sprint goal. |
| `id` | number | Sprint ID. |
| `name` | string | Sprint name. |
| `projectId` | string | Project ID as returned by Leiga. |
| `startDate` | number | Start timestamp. |
| `status` | number | Sprint status. |

## Native endpoint

Through the native Leiga API, this operation is `POST /sprint/add` (base URL `https://app.leiga.com/openapi/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-sprint.md) for the provider-specific parameters and requirements.

