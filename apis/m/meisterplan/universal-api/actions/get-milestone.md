# Meisterplan: Get Milestone

Retrieves a milestone from Meisterplan.

```
GET https://connect.mindcloud.co/v1/universal/meisterplan/latest/actions/get-milestone
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Meisterplan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/meisterplan/latest/actions/get-milestone?connectionId=$CONNECTION_ID&scenarioId=string&projectId=string&milestoneId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "scenarioId": "string",
  "projectId": "string",
  "milestoneId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/meisterplan/latest/actions/get-milestone?${params}`, {
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
| `scenarioId` | string | yes | Internal Meisterplan scenario identifier. |
| `projectId` | string | yes | Internal Meisterplan project identifier. |
| `milestoneId` | string | yes | Internal Meisterplan milestone identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "date": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "name": "Ava Chen",
      "projectPhase": {
        "name": "Ava Chen"
      },
      "status": {
        "value": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `date` | date | Milestone date |
| `id` | string | Milestone ID |
| `name` | string | Milestone name |
| `projectPhase.name` | string | Project phase name |
| `status.value` | string | Milestone status |

## Native endpoint

Through the native Meisterplan API, this operation is `GET /scenarios/:scenarioId/projects/:projectId/milestones/:milestoneId` (base URL `https://api.us.meisterplan.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-milestone.md) for the provider-specific parameters and requirements.

