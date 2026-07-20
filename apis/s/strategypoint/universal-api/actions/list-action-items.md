# Strategypoint: List Action Items

Retrieves action items from Strategypoint.

```
GET https://connect.mindcloud.co/v1/universal/strategypoint/latest/actions/list-action-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Strategypoint `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/strategypoint/latest/actions/list-action-items?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/strategypoint/latest/actions/list-action-items?${params}`, {
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
      "favorite": true,
      "lastEdited": "string",
      "name": "Ava Chen",
      "objectId": 1,
      "ownerId": 1,
      "scorecardId": 1,
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `completed` | boolean | Whether the action item is completed. |
| `favorite` | boolean | Whether the action item is a favorite. |
| `lastEdited` | string | The last-edited timestamp. |
| `name` | string | The action item name. |
| `objectId` | number | The action item identifier. |
| `ownerId` | number | The owning user identifier. |
| `scorecardId` | number | The related scorecard identifier. |
| `type` | string | The ClearPoint element type. |

## Native endpoint

Through the native Strategypoint API, this operation is `GET /actionItems` (base URL `https://app.clearpointstrategy.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-action-items.md) for the provider-specific parameters and requirements.

