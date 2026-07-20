# smapOne: List smap overview

Retrieves smap overview metadata from smapOne.

```
GET https://connect.mindcloud.co/v1/universal/smapOne/latest/actions/list-smap-overview
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a smapOne `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smapOne/latest/actions/list-smap-overview?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smapOne/latest/actions/list-smap-overview?${params}`, {
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
      "categories": [
        {}
      ],
      "id": "string",
      "name": "Ava Chen",
      "smapId": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `categories` | array<object> |  |
| `id` | string |  |
| `name` | string |  |
| `smapId` | string |  |
| `title` | string |  |

## Native endpoint

Through the native smapOne API, this operation is `GET /smaps/overview` (base URL `https://platform.smapone.com/Backend`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-smap-overview.md) for the provider-specific parameters and requirements.

