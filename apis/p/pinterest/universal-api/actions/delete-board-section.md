# Pinterest: Delete Board Section

Deletes an existing board section from Pinterest.

```
DELETE https://connect.mindcloud.co/v1/universal/pinterest/latest/actions/delete-board-section
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pinterest `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/pinterest/latest/actions/delete-board-section?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pinterest/latest/actions/delete-board-section?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Pinterest API returns.

## Native endpoint

Through the native Pinterest API, this operation is `DELETE boards/:boardId/sections/:sectionId` (base URL `https://api.pinterest.com/v5`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-board-section.md) for the provider-specific parameters and requirements.

