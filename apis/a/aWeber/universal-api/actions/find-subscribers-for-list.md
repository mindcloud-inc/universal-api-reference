# AWeber: Find Subscribers For List

Finds subscribers in an AWeber list.

```
GET https://connect.mindcloud.co/v1/universal/aWeber/latest/actions/find-subscribers-for-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AWeber `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aWeber/latest/actions/find-subscribers-for-list?connectionId=$CONNECTION_ID&limit=25&offset=0&accountId=string&listId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "accountId": "string",
  "listId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aWeber/latest/actions/find-subscribers-for-list?${params}`, {
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
| `accountId` | string | yes |  |
| `email` | string | no |  |
| `listId` | string | yes |  |
| `name` | string | no |  |
| `status` | string | no |  |
| `tags` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native AWeber API returns.

## Native endpoint

Through the native AWeber API, this operation is `GET /accounts/:accountId/lists/:listId/subscribers` (base URL `https://api.aweber.com/1.0`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/find-subscribers-for-list.md) for the provider-specific parameters and requirements.

