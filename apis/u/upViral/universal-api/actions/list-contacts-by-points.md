# UpViral: List Contacts By Points

Retrieves campaign contacts from UpViral by points.

```
GET https://connect.mindcloud.co/v1/universal/upViral/latest/actions/list-contacts-by-points
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a UpViral `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/upViral/latest/actions/list-contacts-by-points?connectionId=$CONNECTION_ID&limit=25&offset=0&campaign_id=string&operator=0&points=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "campaign_id": "string",
  "operator": "0",
  "points": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/upViral/latest/actions/list-contacts-by-points?${params}`, {
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
| `campaign_id` | string | yes | The UpViral campaign ID to search contacts in. |
| `operator` | list | yes | Comparison operator for points, such as <, >, or =. One of: `0`, `1`, `2`. |
| `points` | number | yes | Point value to compare against. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native UpViral API returns.

## Native endpoint

Through the native UpViral API, this operation is `POST /` (base URL `https://app.upviral.com/api/v1/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-contacts-by-points.md) for the provider-specific parameters and requirements.

