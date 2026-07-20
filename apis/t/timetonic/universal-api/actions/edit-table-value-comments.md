# Timetonic: Edit Table Value Comments

Updates comments for a table value in Timetonic.

```
PUT https://connect.mindcloud.co/v1/universal/timetonic/latest/actions/edit-table-value-comments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timetonic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/timetonic/latest/actions/edit-table-value-comments" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "bookOwner": "mindcloud",
  "rowId": "147159056",
  "fieldId": "8729209",
  "commentId": "Existing comment id required",
  "comment": "Updated comment text"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/timetonic/latest/actions/edit-table-value-comments', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "bookOwner": "mindcloud",
    "rowId": "147159056",
    "fieldId": "8729209",
    "commentId": "Existing comment id required",
    "comment": "Updated comment text"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `bookOwner` | string | yes | Book owner containing the row. Default: `mindcloud`. |
| `rowId` | string | yes | Row identifier containing the field value. Example: `147159056`. |
| `fieldId` | string | yes | Field identifier whose comment should be edited. Example: `8729209`. |
| `commentId` | string | yes | Comment identifier to edit. Example: `Existing comment id required`. |
| `comment` | string | yes | Updated comment text. Example: `Updated comment text`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Timetonic API returns.

## Native endpoint

Through the native Timetonic API, this operation is `POST` (base URL `https://timetonic.com/live/api.php`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/edit-table-value-comments.md) for the provider-specific parameters and requirements.

