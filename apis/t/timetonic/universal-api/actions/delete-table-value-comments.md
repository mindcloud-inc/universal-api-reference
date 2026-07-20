# Timetonic: Delete Table Value Comments

Deletes comments for a table value from Timetonic.

```
DELETE https://connect.mindcloud.co/v1/universal/timetonic/latest/actions/delete-table-value-comments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timetonic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/timetonic/latest/actions/delete-table-value-comments?connectionId=$CONNECTION_ID&bookOwner=mindcloud&rowId=string&fieldId=string&commentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "bookOwner": "mindcloud",
  "rowId": "string",
  "fieldId": "string",
  "commentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timetonic/latest/actions/delete-table-value-comments?${params}`, {
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
| `bookOwner` | string | yes | Default: `mindcloud`. |
| `rowId` | string | yes |  |
| `fieldId` | string | yes |  |
| `commentId` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Timetonic API returns.

## Native endpoint

Through the native Timetonic API, this operation is `POST` (base URL `https://timetonic.com/live/api.php`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-table-value-comments.md) for the provider-specific parameters and requirements.

