# Strategypoint: List Goals

Retrieves goals from Strategypoint.

```
GET https://connect.mindcloud.co/v1/universal/strategypoint/latest/actions/list-goals
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Strategypoint `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/strategypoint/latest/actions/list-goals?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/strategypoint/latest/actions/list-goals?${params}`, {
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
| `count` | number | no | Maximum number of records to return. |
| `lastEdited` | string | no | Filter by last-edited timestamp. |
| `lastEditedBy` | number | no | Filter by the user who last edited the record. |
| `order` | string | no | Sort order for the result set. |
| `page` | number | no | Page number to return. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "completed": true,
      "goalId": 1,
      "name": "Ava Chen",
      "object": "string",
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
| `goalId` | number | The unique goal identifier. |
| `name` | string | The goal name. |
| `object` | string | The ClearPoint object type. |
| `ownerId` | number | The owning user identifier. |
| `percentComplete` | number | Percent completion for the goal. |
| `periodId` | number | The related period identifier. |
| `statusId` | number | The goal status identifier. |

## Native endpoint

Through the native Strategypoint API, this operation is `GET /goals` (base URL `https://app.clearpointstrategy.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-goals.md) for the provider-specific parameters and requirements.

