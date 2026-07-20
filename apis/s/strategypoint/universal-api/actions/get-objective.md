# Strategypoint: Get Objective

Retrieves an objective from Strategypoint.

```
GET https://connect.mindcloud.co/v1/universal/strategypoint/latest/actions/get-objective
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Strategypoint `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/strategypoint/latest/actions/get-objective?connectionId=$CONNECTION_ID&objectiveId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "objectiveId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/strategypoint/latest/actions/get-objective?${params}`, {
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
| `objectiveId` | number | yes | The unique objective identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "completed": true,
      "description": "string",
      "favorite": true,
      "lastEdited": "string",
      "name": "Ava Chen",
      "objectId": 1,
      "ownerId": 1,
      "scorecardId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `completed` | boolean | Whether the objective is completed. |
| `description` | string | The objective description. |
| `favorite` | boolean | Whether the objective is a favorite. |
| `lastEdited` | string | The last-edited timestamp. |
| `name` | string | The objective name. |
| `objectId` | number | The objective identifier. |
| `ownerId` | number | The owning user identifier. |
| `scorecardId` | number | The related scorecard identifier. |

## Native endpoint

Through the native Strategypoint API, this operation is `GET /objectives/{objectiveId}` (base URL `https://app.clearpointstrategy.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-objective.md) for the provider-specific parameters and requirements.

