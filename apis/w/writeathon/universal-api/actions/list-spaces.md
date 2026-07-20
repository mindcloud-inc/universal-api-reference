# Writeathon: List Spaces

Retrieves the user's spaces from Writeathon.

```
GET https://connect.mindcloud.co/v1/universal/writeathon/latest/actions/list-spaces
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Writeathon `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/writeathon/latest/actions/list-spaces?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/writeathon/latest/actions/list-spaces?${params}`, {
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
      "data": [
        {
          "author": "string",
          "cover": "string",
          "created": "string",
          "description": "string",
          "emojiIcon": "string",
          "id": "string",
          "order": 1,
          "status": 1,
          "style": "string",
          "title": "string",
          "updated": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> |  |
| `data[].author` | string |  |
| `data[].cover` | string |  |
| `data[].created` | string |  |
| `data[].description` | string |  |
| `data[].emojiIcon` | string |  |
| `data[].id` | string |  |
| `data[].order` | number |  |
| `data[].status` | number |  |
| `data[].style` | string |  |
| `data[].title` | string |  |
| `data[].updated` | string |  |

## Native endpoint

Through the native Writeathon API, this operation is `GET /v1/users/{{credentials.userId}}/spaces` (base URL `https://api.writeathon.cn`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-spaces.md) for the provider-specific parameters and requirements.

