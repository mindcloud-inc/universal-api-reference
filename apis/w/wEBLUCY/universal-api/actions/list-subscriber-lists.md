# WEBLUCY: List Subscriber Lists

Retrieves subscriber lists from WEBLUCY.

```
GET https://connect.mindcloud.co/v1/universal/wEBLUCY/latest/actions/list-subscriber-lists
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WEBLUCY `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wEBLUCY/latest/actions/list-subscriber-lists?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wEBLUCY/latest/actions/list-subscriber-lists?${params}`, {
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
      "clicks": 1,
      "created": 1,
      "id": 1,
      "name": "Ava Chen",
      "opens": 1,
      "subscribers": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `clicks` | number |  |
| `created` | number |  |
| `id` | number |  |
| `name` | string |  |
| `opens` | number |  |
| `subscribers` | number |  |

## Native endpoint

Through the native WEBLUCY API, this operation is `GET /subscriber-lists` (base URL `https://apps.weblucy.com/api/site`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-subscriber-lists.md) for the provider-specific parameters and requirements.

