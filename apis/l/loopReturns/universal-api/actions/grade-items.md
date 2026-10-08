# Loop Returns: Grade Items

Grade the condition of return line items.

```
PUT https://connect.mindcloud.co/v1/universal/loopReturns/latest/actions/grade-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Loop Returns `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/loopReturns/latest/actions/grade-items" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "items[].line_item_id": 1,
  "items[].description": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/loopReturns/latest/actions/grade-items', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "items[].line_item_id": 1,
    "items[].description": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `items[]` | array<object> | no | An array of items to grade. Max 30 items per request. |
| `items[].line_item_id` | number | yes | (required) The unique identifier associated with the line item. |
| `items[].description` | string | yes | The description of the item's condition. Max 255 characters. |
| `items[].condition_category` | list<string> | no | The condition of the returned item. Available options: `grade_a`, `grade_b`, `grade_c`, `grade_d`, `incorrect_item`, `missing, junk` |
| `items[].return_processor` | string | no | The email address of the warehouse partner used to process returns. Max 100 characters. |
| `items[].note` | string | no | Any additional notes on the item's condition. |
| `items[].images[]` | array<string> | no | Add up to 5 images to show the items condition. Max 5 URLs Max 2048 characters. |
| `items[].inspected_at` | string | no | The date and time at which the item was inspected, using the ISO 8601 date format. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Loop Returns API returns.

## Native endpoint

Through the native Loop Returns API, this operation is `POST https://api.loopreturns.com/api/v1/dispositioning/grade` (base URL `https://api.loopreturns.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/grade-items.md) for the provider-specific parameters and requirements.

