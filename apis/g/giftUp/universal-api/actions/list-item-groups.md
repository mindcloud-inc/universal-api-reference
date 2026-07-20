# Gift Up: List Item Groups



```
GET https://connect.mindcloud.co/v1/universal/giftUp/latest/actions/list-item-groups
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Gift Up `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/giftUp/latest/actions/list-item-groups?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/giftUp/latest/actions/list-item-groups?${params}`, {
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
      "autoExpand": true,
      "description": "string",
      "id": "string",
      "name": "Ava Chen",
      "sortOrder": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `autoExpand` | boolean |  |
| `description` | string |  |
| `id` | string |  |
| `name` | string |  |
| `sortOrder` | number |  |

## Native endpoint

Through the native Gift Up API, this operation is `GET /groups` (base URL `https://api.giftup.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-item-groups.md) for the provider-specific parameters and requirements.

