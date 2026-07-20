# Strategypoint: Get Initiative

Retrieves an initiative from Strategypoint.

```
GET https://connect.mindcloud.co/v1/universal/strategypoint/latest/actions/get-initiative
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Strategypoint `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/strategypoint/latest/actions/get-initiative?connectionId=$CONNECTION_ID&initiativeId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "initiativeId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/strategypoint/latest/actions/get-initiative?${params}`, {
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
| `initiativeId` | number | yes | The unique initiative identifier. |

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
| `completed` | boolean | Whether the initiative is completed. |
| `description` | string | The initiative description. |
| `favorite` | boolean | Whether the initiative is a favorite. |
| `lastEdited` | string | The last-edited timestamp. |
| `name` | string | The initiative name. |
| `objectId` | number | The initiative identifier. |
| `ownerId` | number | The owning user identifier. |
| `scorecardId` | number | The related scorecard identifier. |

## Native endpoint

Through the native Strategypoint API, this operation is `GET /initiatives/{initiativeId}` (base URL `https://app.clearpointstrategy.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-initiative.md) for the provider-specific parameters and requirements.

