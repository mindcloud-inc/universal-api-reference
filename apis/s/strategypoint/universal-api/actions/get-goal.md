# Strategypoint: Get Goal

Retrieves a goal from Strategypoint.

```
GET https://connect.mindcloud.co/v1/universal/strategypoint/latest/actions/get-goal
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Strategypoint `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/strategypoint/latest/actions/get-goal?connectionId=$CONNECTION_ID&goalId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "goalId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/strategypoint/latest/actions/get-goal?${params}`, {
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
| `goalId` | number | yes | The unique goal identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "completed": true,
      "description": "string",
      "goalId": 1,
      "name": "Ava Chen",
      "ownerId": 1,
      "percentComplete": 1,
      "periodId": 1,
      "statusId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `completed` | boolean | Whether the goal is completed. |
| `description` | string | The goal description. |
| `goalId` | number | The unique goal identifier. |
| `name` | string | The goal name. |
| `ownerId` | number | The owning user identifier. |
| `percentComplete` | number | Percent completion for the goal. |
| `periodId` | number | The related period identifier. |
| `statusId` | number | The goal status identifier. |

## Native endpoint

Through the native Strategypoint API, this operation is `GET /goals/{goalId}` (base URL `https://app.clearpointstrategy.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-goal.md) for the provider-specific parameters and requirements.

