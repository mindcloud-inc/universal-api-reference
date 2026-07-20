# HyperDone: List Board Members



```
GET https://connect.mindcloud.co/v1/universal/hyperDone/latest/actions/list-board-members
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HyperDone `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hyperDone/latest/actions/list-board-members?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hyperDone/latest/actions/list-board-members?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `name` | string |  |

## Native endpoint

Through the native HyperDone API, this operation is `GET /GetBoardMembers` (base URL `https://hyperdone.com/api/public`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-board-members.md) for the provider-specific parameters and requirements.

