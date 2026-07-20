# Watbot: Delete List Item

Deletes an existing list item from Watbot.

```
DELETE https://connect.mindcloud.co/v1/universal/watbot/latest/actions/delete-list-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Watbot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/watbot/latest/actions/delete-list-item?connectionId=$CONNECTION_ID&itemId=5dee62e46637df57be7bc686" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "itemId": "5dee62e46637df57be7bc686"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/watbot/latest/actions/delete-list-item?${params}`, {
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
| `itemId` | string | yes | ID of the list item. Example: `5dee62e46637df57be7bc686`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Watbot API returns.

## Native endpoint

Through the native Watbot API, this operation is `POST /deleteListItem` (base URL `https://watbot.ru/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-list-item.md) for the provider-specific parameters and requirements.

